Berikut adalah penjelasan masing2 baris kode di script

wget https://github.com/labusiam/dataset/raw/main/weather_data.xlsx -> buat download file yang dimaksud

in2csv weather_data.xlsx --sheet "weather_2014" > weather_2014.csv -> convert ke csv
in2csv weather_data.xlsx --sheet "weather_2015" > weather_2015.csv -> convert ke csv

csvstack weather_2014.csv weather_2015.csv > weather.csv -> gabungin kedua file csv menjadi satu

rm weather_data.xlsx -> hapus file

cat weather.csv | sample -r 0.3 > sample_weather.csv -> bikin sample file

