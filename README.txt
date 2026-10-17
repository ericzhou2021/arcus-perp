Arcus SPY/QQQ 对冲机器人

策略：看 SPY 5分钟 RSI12，低于45做多SPY，高于55做空SPY，同时开等额反向QQQ。SPY盈利0.3%两边一起平。每边名义金额约等于权益×5。挂单偏移约1档（0.001%）。

安装：Python 3.10+，pip install -r requirements.txt
填写：wallet_address 和 api_signing_key（API Signing Key，不是钱包私钥），或环境变量 ARCUS_WALLET_ADDRESS / ARCUS_SIGNING_KEY。
子账户：account_index 改成对应编号，Key 必须在该子账户下生成。先在交易所设好全仓杠杆。
运行：先保持 dry_run=true，python -u bot.py。确认后再改 false。
注意：不要在这个子账户手动下单。runtime 文件夹不要删。实盘有爆仓风险。
