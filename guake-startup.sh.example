sudo service postgresql stop
guake -n guake -e 'cd ~/Projects/wayup && docker-compose up' guake -r 'tcj_docker'
guake -n guake -e 'cd ~/Projects/TCJ/frontend-dev && grunt serve' guake -r 'tcj_an'
guake -n guake -e 'cd ~/Projects/TCJ/website && npm start' guake -r 'tcj_r'
guake -n guake -e 'cd ~/Projects/TCJ/ && source venv/bin/activate && python manage.py runserver' guake -r 'tcj_back'
guake -n guake -e 'cd ~/Projects/TCJ/ && source venv/bin/activate && python manage.py shell_plus' guake -r 'tcj_sh'

