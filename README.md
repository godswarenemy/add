journalctl -u andromedad -f -o cat
systemctl restart andromedad
curl localhost:26657/status
curl -s localhost:26657/status | jq .result.sync_info.catching_up
andromedad keys show wallet --bech val -a
andromedad tx staking delegate YOUR_VALOPER_ADDRESS 1000000uandr --from wallet --chain-id $CHAIN_ID --fees 5000uandr
