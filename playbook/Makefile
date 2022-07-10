.PHONY: play
play:
	ansible-playbook -i ./hosts -u isucon site.yml -t nginx --start-at="cp sites-available/default" --check
