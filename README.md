#  Enabling and Applying cust-edx.org Theme

## Step 1: Cloning the theme

    mkdir /edx/app/edxapp/themes && cd /edx/app/edxapp/themes  
    git clone https://github.com/hossam92/cust-edx.org.git  
    chown -R edxapp:edxapp /edx/app/edxapp/themes  
    chmod -R u+rw /edx/app/edxapp/themes  

## Step 2: Enabling the theme for LMS  
Edit /edx/app/edxapp/lms.env.json to set:     
    
    "ENABLE_COMPREHENSIVE_THEMING": true,  
    "COMPREHENSIVE_THEME_DIRS": [  
        "/edx/app/edxapp/themes"  
    ],  
    "THEME_NAME": "cust-edx.org"  

## Step 3: Applying the theme  
1- Sign in to the Django administration console for your base URL. For example, http://{your_URL}/admin.  
2- Select Site themes.  
3- Select Add site theme.  
4- From the Site menu, select the site you want to apply a theme to.  
5- In the Theme dir name field, enter the identifier of the theme, which is "cust-edx.org".  
6- Select Save.  
