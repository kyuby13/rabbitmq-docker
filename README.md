# rabbitmq-docker

Rabbitmq untuk docker compose

# Run

docker-compose up -d
# Login Dashboard

http://localhost:15672 | http://IPADDR:15672 user : guest pass : guest
# Publishing a Message With Go

Install library go get github.com/streadway/amqp. 

go run sendMessage.go 

cek queue di dashboard
# Reading Messages With Go

run consume.go

# Dinamic publish message

Tambahkan command berikut ke line paling atas di file sendMessage.go

// Let's catch the message from the terminal.

reader := bufio.NewReader(os.Stdin)

fmt.Println("What message do you want to send?")

mPayload, _ := reader.ReadString('\n')
