##### `Thread `
Cách xem số core: gõ  `"lscpu"` trong terminal sẽ cho kết quả như sau:
```
Thread(s) per core:    2
Core(s) per socket:    12
Socket(s):             4
```
Như trên ta có (4 * 12 * 2) = 96 threads

### ` Chạy bằng NodeJs `
Cách cài Nodejs [ở đây](https://nodejs.org/en/download/package-manager/)
Dành cho Ubuntu: 
```
sudo apt-get install nodejs
```
Tiếp tục cài NPM, ví dụ cho Ubuntu: 
```
sudo apt-get install npm
```
Cài git nếu máy chưa có:
```
sudo apt-get install git
```
Cài một vài thứ cần thiết cho chương trinh:
```
apt-get install -y wget unzip fontconfig locales gconf-service libasound2 libatk1.0-0 libc6 libcairo2 libcups2 libdbus-1-3 libexpat1 libfontconfig1 libgcc1 libgconf-2-4 libgdk-pixbuf2.0-0 libglib2.0-0 libgtk-3-0 libnspr4 libpango-1.0-0 libpangocairo-1.0-0 libstdc++6 libx11-6 libx11-xcb1 libxcb1 libxcomposite1 libxcursor1 libxdamage1 libxext6 libxfixes3 libxi6 libxrandr2 libxrender1 libxss1 libxtst6 ca-certificates fonts-liberation libappindicator1 libnss3 lsb-release xdg-utils wget

```
Chạy tiếp command sau
```
git clone https://github.com/sgorki/banano.miner.git miner && \
	cd miner && \
	npm i --only=prod && \
	npm i --save puppeteer@1.16.0
```

Sau khi chạy xong lênh trên thì chạy lệnh sau để đào Banano :
```
node index.js <Địa chỉ Banano> <Số core> coinimp
```
Ví dụ
```
node index.js ban_1xm7hxubujqgsezxqb6dwd7zarskdiahdcspmhqqtzi177qzpsqzq6df7rg5 6 coinimp

```
### `Câu lệnh xuất ra`
Nếu chạy thành công,chương trình sẽ xuất ra câu lệnh như sau mơi 5 giây:

```
console 64.4/Hps, session: (0.05334BAN, 1778/H), 24h estimate 166.92480000000003BAN
```
Cứ 5 phút bạn sẽ nhận được stats của account
```
dc754b618731c8924aefb61b51e18728 {
	account: 'ban_1xm7hxubujqgsezxqb6dwd7zarskdiahdcspmhqqtzi177qzpsqzq6df7rg5',
	hashes: 39736133,
	balance: 0.48384
}
```
