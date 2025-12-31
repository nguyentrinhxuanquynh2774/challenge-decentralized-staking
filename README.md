# ĐỒ ÁN CHALLENGE 1: DECENTRALIZED STAKING

## Introduction

Dự án này là lời giải cho **Challenge 1: Decentralized Staking** thuộc hệ sinh thái **SpeedRunEthereum**.  
Bài tập tập trung vào việc xây dựng một **Smart Contract staking ETH**, có quản lý **ngưỡng mục tiêu (Threshold)** và **thời gian kết thúc (Deadline)**.

### Các tính năng đã hoàn thành
- **Stake:** Cho phép người dùng gửi ETH vào Smart Contract.
- **Quản lý trạng thái:** Tự động tính toán Deadline và kiểm tra ngưỡng Threshold.
- **Execute:** Chuyển toàn bộ ETH sang `ExampleExternalContract` nếu đạt mục tiêu đúng hạn.
- **Withdraw:** Cho phép người dùng rút lại ETH nếu không đạt Threshold sau khi hết Deadline.

---

## Yêu cầu môi trường 

Để chạy dự án, máy tính cần cài đặt:
- **NodeJS** (v16.x hoặc mới hơn)
- **Yarn** (khuyến nghị)
- **Git**
- **Trình duyệt Chrome**
- **Ví MetaMask**

---

## Hướng dẫn chạy 

Mở **3 cửa sổ Terminal riêng biệt** và chạy các lệnh sau theo đúng thứ tự.

### Bước 1: Cài đặt thư viện và chạy Blockchain cục bộ (Hardhat Node)
```bash
yarn install
yarn chain
```
### Bước 3: Triển khai Smart Contract lên Localhost
```bash
yarn deploy
```
### Bước 4: Khởi chạy giao diện người dùng (Frontend)
```bash
yarn start
```
### Bước 5: Truy cập: http://localhost:3000 để tương tác.

## ⚙️ Cấu hình mạng & Triển khai (Deployment)

Dự án hỗ trợ linh hoạt giữa môi trường **Local** và **Testnet**, phù hợp cho cả mục đích học tập và triển khai thực tế.

---

### Môi trường chấm bài (Local)

- Dự án được cấu hình mặc định chạy trên **Hardhat local blockchain**.
- Cấu hình này nằm trong file `scaffold.config.ts`:

```ts
targetNetworks: [chains.hardhat]


