## Ön Bilgi
- Aleo zor bir testnet önceki testnette de büyük zorluklar çıkmıştı ve istediği sistem de bizim katıldığımız standart node testlerinin çok üstünde, bunu göze alarak girin. Videonun ilk bölümlerinde önemli açıklamarı yapıyorum, mutlaka bakın. Sonunda ödül de kazanamayabilirsiniz. 

## Sistem Gereksinimleri
 - CPU: 16-cores (32-cores önerilen)
 - RAM: 16GB of memory (32GB önerilen)
 - HDD: 128GB of disk space
 - Network: 10 Mbps of upload and download bandwidth
 
## Güncellemeler
```
sudo apt update
sudo apt install make clang pkg-config libssl-dev build-essential gcc xz-utils git curl vim tmux ntp jq llvm ufw -y
```
## Rust Yüklemek
```
curl --proto '=https' --tlsv1.2 -sSf https://sh.rustup.rs | sh -s -- -y
source $HOME/.cargo/env
```
## Portlar
```
sudo ufw allow 4133/tcp
sudo ufw allow 3033/tcp
```
## Node Dosyaları
```
tmux
git clone https://github.com/AleoHQ/snarkOS.git --depth 1
cd snarkOS
./build_ubuntu.sh
cargo install --path .
```
## Cüzdan Oluşturmak
- Alttaki kodu girdiğinizde size verilen bilgileri kesinlikle kaydedin.
```
snarkos account new
```
```
 Attention - Remember to store this account private key and view key.

  Private Key  APrivateKey1xxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxx  <-- Save Me And Use In The Next Step
     View Key  AViewKey1xxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxx  <-- Save Me
      Address  aleo1xxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxx  <-- Save Me
```
## Node Başlatmak
- Aşağıdaki kodu girdiğinizde çıkan ekranda sizden cüzdanınızın Private Key'ini girmenizi istiyor.
```
./run-prover.sh
```
- Bu adımla birlikte node çalışmaya başlıyor. Cüzdanınızın topladığı kredileri bu adreslerden aratarak bulabilirsiniz. 
  - https://www.aleo.network/ & https://aleo123.io/ & https://explorer.hamp.app/
