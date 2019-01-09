# Belly Button Biodiversity

Issues to keep in mind when running this app, or trying to replicate:

1.  When checking the "https://localhost:5000/metadata/<sample>" or "/samples/<sample>" URLs, manually enter a valid number
 you can select from the drop down on index.html in the place of <sample>.  It will not dynamically pull the sample number selected.
2.  Chrome did not render the Plotly charts at first until I restarted my machine.  Not sure what was going on, but Chrome can have 
issues with D3/Plotly.  FireFox always worked.
3.  Although I generated a requirements.txt file from GitBash ("pip freeze > requirements"), it did not include gunicorn on the 
first try.  I had heroku issues so I had to run that command again to include gunicorn in the file and push to heroku again.
4.  When I pushed to heroku, the configuration was cached from the previous push, so it did not work initially.  It only worked by
deleting the heroku app and re-init/add/commit/push to the new heroku app.