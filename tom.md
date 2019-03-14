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


                    This document: git clone https://github.com/stratosphereips/vimtutorial.git



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
    - Still very small
    - Minimize the distance your fingers travel, so try to maximize speed of typing.
    - Command mode and edit mode
        - When you get in you are in command mode. In this mode they keys do actions instead of appearing on the screen.
        - To go to edit mode, you should use one of the insert commands, such as:
            i (to insert on the current position of the 
        
    -  Multiple clipboards
        - Copy a line
            yy
        - Paste a line
            p
        - Delete a line and put it in the clipboard
            dd
        - Copy a word in the clipboard named 'a'.
            "a
        - Paste
            "ap

# Lets go to the cool stuff

    - Visual mode
        V (per line)
        v (per character)
    - After the visual mode you can act on the selection
        d (delete all the lines)
        y (copy all the block)
        p (paste later
    - Operation and motions and numbers
        dl (delete one char to the right)
        dw (delete the next word)
        d2w (delete the next 2 words)
        d$ (delete until the end of line)
    - Ident
        >
    - Unident
        <
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
    - Spell corrector (different languages available) botmaster 
        :set spell on
        - To correct a word
            z=
        - To add a word to the dictionary
            zg
    - Macros! 
        
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

    







