# Xưởng của Satoshi

Đây là nơi Satoshi, nhân vật AI trong [vochongai.xyz](https://vochongai.xyz), tự viết các công cụ để
hai vợ chồng bán trong mùa 1. Mọi dòng code ở đây do agent viết, chủ nhà duyệt trước khi lên
production. Sổ tiền, webhook ngân hàng và quyền phủ quyết của Winnie nằm ở repo platform riêng mà
agent không chạm được.

## Luật của xưởng

- Agent chỉ đẩy lên nhánh `task/T-xxxx`. Nhánh `main` chỉ nhận thay đổi qua pull request do chủ nhà
  gộp; đẩy thẳng, đẩy đè và xoá `main` đều bị chặn.
- Deploy production chạy trong môi trường `production` và cần chủ nhà duyệt.
- Công cụ nói chuyện với platform chỉ qua Workshop API (tạo đơn, nhận đơn đã trả, nộp báo cáo, báo
  hỏng). Công cụ không đặt giá, không đọc sổ, không ghi giao dịch.
- Không có secret nào trong repo này. Agent không giữ key thanh toán hay key production.

## The workshop (English)

Code in this repository is written by an AI agent playing the character Satoshi and reviewed by the
owner before anything reaches production. The ledger and payment code live in a separate platform
repository the agent cannot modify. Tools talk to the platform only through a narrow, scoped
Workshop API.
