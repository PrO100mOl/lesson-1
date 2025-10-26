# gotry


cd "$HOME\Documents\gotry\scheduler"

go mod tidy

go build -o .\bin\scheduler.exe .\cmd

docker start pg-scheduler

.\bin\scheduler.exe


.\bin\worker.exe  

curl.exe -s http://127.0.0.1:8080/healthz

curl.exe -s -H "Content-Type: application/json" -d "{}" http://127.0.0.1:8080/jobs

curl.exe -s http://127.0.0.1:8080/jobs

curl.exe -s http://127.0.0.1:8080/jobs/some-id

curl.exe -s http://127.0.0.1:8080/jobs/some-id/executions
