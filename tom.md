#                                           Thursdays of Malware 2019/03/13


                                                         Vi


                                                   ..  .....                           
                                              ....,,,,,,,,,,,,,,,.                     
                                          ...  ......,,,,,,,,,......                   
                                        ...      ................                      
                                      ...            .........                         
                                    ...                                                
                                   ..            *((###((((/(##((/.                    
                                  ..         *//.  .,,,,,,,,,,,.   */*                 
                                 ..       ,*  ,,,,,,,,,,,,,,,,,,,,,,,. *,              
                                ..      ..  .,,,,,,,,,,,,,,,,,,,,,,,,,.  ..            
                               ..      .      ,,,,,,,,,,,,,,,,,,,,,,,      .           
                               ..      .,,*@    ,,,,,,,,,,,,,,,,,,,    &/,,,           
                               ..     .,,,,(@@%   ,,,,,,,,,,,,,,,   #@@#,,,,,          
                               ..     ,,,,,,(@@@@. .,,,,,,,,,,,   @@@@#,,,,,,.         
                               ..    ,,,,,,,,,@@,  ,&.,,,,,,,.%   .@@*,,,,,,,,         
                               ..     .,,,,,,,,,,,,,,,,,,,,,,,,,,,,,,,,,,,,,           
                               ..        .,,,,,,,,,,,,,,,,,,,,,,,,,,,,,,.              
                                ..              .,,,,,,,,,,,,,,,,,.                    
                                 ..            ..,,,,,,,,,,,,,,,,,..                   
                                 ...                                                   
                                  ...                                           .      
                                    ..                                        .        
                                     ...                                    ..         
                                       ....                              ...           
                                          .....                      ....              
                                             .........................                 
                                                  .,,**/////**,..                      
                                      ,,,,,,,,,,,*%(,         ,#%#,,,,,,,,,,,          



# This class in one command

    vimtutor 



# Intro to Vi

- What is vi?
    
    An editor with huge amount of features. Think of it as a new languague. Its hard at the beggining.

- How to get in
    vi file

- Get out by saving. If you didn't modify, its OK also.
    ZZ

- Get out without saving (! means force quit)
    :q!

- If you didn't make any modifications, get out
    :q

- Why Vi?
    - Ubiquitous. Its installed in most Linux/Macos systems. Windows can have it.
    - Still small
    - Minimize the distance your fingers travel, so try to maximize speed of typing.
    - Command mode and edit mode
        
    -  Multiple clipboards


# Lets go to the cool stuff

    - Undo
        u
        g-
    - Redo
        CTRL-T
        g+
    - Go back to the location of the last edit: 
        g;
    - Go back to the state of the document 1 minute ago?
        :earlier 1m
    - Super search
        - Search for test
            /test
        - Delete test
            d/test
    - Status about the file
        g CTRL-g

# Getting serious

- Operation and motions

    dl (delete one char to the right)
    dw (delete the next word)
    d$ (delete until the end of line)

- Spell corrector (different languages available) botmaster 
    :set spell on
    - To correct a word
        z=
    - To add a word to the dictionary
        zg
        


# Features

- Edit compressed files
    - echo "sdf" > test
    - gzip test
    - vi test.gz


# Plugins
    - Vundle


# Configuration file
    ~/.vimrc
        - Put
            syntax on
            set background=dark
            set hlsearch
            set tabstop=4
            set shiftwidth=4
            set expandtab

# Folding

    Put this in your ~/.vimrc
        nnoremap <silent> <Space> @=(foldlevel('.')?'za':"\<Space>")<CR>
        vnoremap <Space> zf

    







