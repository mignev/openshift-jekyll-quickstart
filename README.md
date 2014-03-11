# So what is Jekyll, exactly?

Jekyll is a simple, blog-aware, static site generator. It takes a template directory containing raw text files in various formats, runs it through Markdown (or Textile) and Liquid converters, and spits out a complete, ready-to-publish static website suitable for serving with your favorite web server. Jekyll also happens to be the engine behind GitHub Pages, which means you can use Jekyll to host your project’s page, blog, or website from GitHub’s servers for free. More info you can find here: http://jekyllrb.com/

# Running on OpenShift

Create an account at http://openshift.redhat.com/

Create a Openshift application (using any application name you want)

    rhc app create myjekyll ruby-1.9 --from-code=https://github.com/mignev/openshift-jekyll-quickstart.git
  
If you want to add Jekyll to an existing project, go to the project dir.

    cd myproject
    git remote add jekyll -m master https://github.com/mignev/openshift-jekyll-quickstart.git
    git pull -s recursive -X theirs jekyll master

Then push the repo usptream

    git push
  
That's it! Now you have Jekyll on OpenShift :) Enjoy!

# License

This code is dedicated to the public domain to the maximum extent permitted by applicable law, pursuant to CC0 (http://creativecommons.org/publicdomain/zero/1.0/)


[![Bitdeli Badge](https://d2weczhvl823v0.cloudfront.net/mignev/openshift-jekyll-quickstart/trend.png)](https://bitdeli.com/free "Bitdeli Badge")

