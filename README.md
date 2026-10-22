```asm
BITS 32

section .data

welcome db "=======================================", 10
    db "       THE MYSTIC ZODIAC ORACLE", 10
    db "=======================================", 10
    db "       *       /\       *", 10
    db "              /  \", 10
    db "        *    /____\    *", 10
    db "              |  |", 10
    db "              |__|", 10
    db "        DISCOVER YOUR DESTINY!", 10
    db "=======================================", 10
    db "Fictional predictions for entertainment.", 10
    db 10
    db 0

name_prompt db "Enter your name (1-63 characters): ", 0
month_prompt db "Enter birth month (1-12): ", 0
day_prompt db "Enter birth day: ", 0

bad_name db "Please enter a nonblank name of at most 63 characters.", 10
    db 0

bad_month db "Invalid month. Enter a number from 1 to 12.", 10
    db 0

bad_date db "Invalid date. Check the month length (February has 28 days).", 10
    db 0

hello db 10
    db "Welcome, ", 0

bang db "!", 10
    db 0

menu db 10
    db "[1] Love and Relationships", 10
    db "[2] Career and Studies", 10
    db "[3] Health and Wellness", 10
    db "[4] Lucky Number and Color", 10
    db "[5] View Zodiac Information", 10
    db "[6] Exit", 10
    db "Enter your choice: ", 0

bad_menu db "Invalid selection. Choose 1-6.", 10
    db 0

again db 10
    db "Return to menu? (Y/N): ", 0

bad_again db "Please enter Y or N.", 10
    db 0

bye db 10
    db "Thank you for visiting the Mystic Zodiac Oracle!", 10
    db 0

love db "LOVE AND RELATIONSHIPS", 10
    db "A thoughtful conversation may strengthen a connection today.", 10
    db 0

career db "CAREER AND STUDIES", 10
    db "Your strengths can help you solve a difficult problem today.", 10
    db "Stay focused and confident!", 10
    db 0

health db "HEALTH AND WELLNESS", 10
    db "A calm break and a balanced routine may refresh your energy.", 10
    db 0

heading db 10
    db "=======================================", 10
    db "           YOUR ZODIAC SIGN", 10
    db "=======================================", 10
    db 0

sign0 db "Zodiac Sign: CAPRICORN", 10
    db "Element: Earth", 10
    db "Symbol: Sea Goat", 10
    db "Personality: Patient, disciplined, responsible.", 10
    db 0

art0 db "  /\  /\", 10
    db " (  oo  )", 10
    db "  /|__|\", 10
    db 0

lucky0 db "Lucky number: 8", 10
    db "Lucky color: Brown", 10
    db 0

sign1 db "Zodiac Sign: AQUARIUS", 10
    db "Element: Air", 10
    db "Symbol: Water Bearer", 10
    db "Personality: Independent, inventive, friendly.", 10
    db 0

art1 db "   ~ ~ ~", 10
    db "  (____)", 10
    db "   /  \", 10
    db 0

lucky1 db "Lucky number: 11", 10
    db "Lucky color: Blue", 10
    db 0

sign2 db "Zodiac Sign: PISCES", 10
    db "Element: Water", 10
    db "Symbol: Fish", 10
    db "Personality: Compassionate, imaginative, gentle.", 10
    db 0

art2 db " ><(((>   <)))><", 10
    db 0

lucky2 db "Lucky number: 7", 10
    db "Lucky color: Sea green", 10
    db 0

sign3 db "Zodiac Sign: ARIES", 10
    db "Element: Fire", 10
    db "Symbol: Ram", 10
    db "Personality: Brave, energetic, determined.", 10
    db 0

art3 db "  (o)  (o)", 10
    db "   \__/", 10
    db "   /oo\", 10
    db 0

lucky3 db "Lucky number: 9", 10
    db "Lucky color: Red", 10
    db 0

sign4 db "Zodiac Sign: TAURUS", 10
    db "Element: Earth", 10
    db "Symbol: Bull", 10
    db "Personality: Reliable, patient, practical.", 10
    db 0

art4 db "  \    /", 10
    db "   (oo)", 10
    db "   /__\", 10
    db 0

lucky4 db "Lucky number: 6", 10
    db "Lucky color: Green", 10
    db 0

sign5 db "Zodiac Sign: GEMINI", 10
    db "Element: Air", 10
    db "Symbol: Twins", 10
    db "Personality: Curious, expressive, adaptable.", 10
    db 0

art5 db "  O   O", 10
    db " /|\ /|\", 10
    db " / \ / \", 10
    db 0

lucky5 db "Lucky number: 5", 10
    db "Lucky color: Yellow", 10
    db 0

sign6 db "Zodiac Sign: CANCER", 10
    db "Element: Water", 10
    db "Symbol: Crab", 10
    db "Personality: Caring, intuitive, protective.", 10
    db 0

art6 db " \  o o  /", 10
    db "  (_____)", 10
    db " / /   \ \", 10
    db 0

lucky6 db "Lucky number: 2", 10
    db "Lucky color: Silver", 10
    db 0

sign7 db "Zodiac Sign: LEO", 10
    db "Element: Fire", 10
    db "Symbol: Lion", 10
    db "Personality: Confident, creative, courageous.", 10
    db 0

art7 db "   /\_/\", 10
    db "  ( o.o )", 10
    db "   > ^ <", 10
    db 0

lucky7 db "Lucky number: 1", 10
    db "Lucky color: Gold", 10
    db 0

sign8 db "Zodiac Sign: VIRGO", 10
    db "Element: Earth", 10
    db "Symbol: Maiden", 10
    db "Personality: Analytical, helpful, organized.", 10
    db 0

art8 db "    O", 10
    db "   /|\", 10
    db "   / \", 10
    db 0

lucky8 db "Lucky number: 4", 10
    db "Lucky color: Navy blue", 10
    db 0

sign9 db "Zodiac Sign: LIBRA", 10
    db "Element: Air", 10
    db "Symbol: Scales", 10
    db "Personality: Fair, diplomatic, sociable.", 10
    db 0

art9 db "    |", 10
    db " ---+---", 10
    db " (_) (_)", 10
    db "    |", 10
    db 0

lucky9 db "Lucky number: 6", 10
    db "Lucky color: Pink", 10
    db 0

sign10 db "Zodiac Sign: SCORPIO", 10
    db "Element: Water", 10
    db "Symbol: Scorpion", 10
    db "Personality: Passionate, resourceful, loyal.", 10
    db 0

art10 db "  __   _", 10
    db " (oo)_/ )", 10
    db " /||\  /", 10
    db 0

lucky10 db "Lucky number: 9", 10
    db "Lucky color: Maroon", 10
    db 0

sign11 db "Zodiac Sign: SAGITTARIUS", 10
    db "Element: Fire", 10
    db "Symbol: Archer", 10
    db "Personality: Optimistic, adventurous, honest.", 10
    db 0

art11 db "  O    )", 10
    db " /|---)>", 10
    db " / \   )", 10
    db 0

lucky11 db "Lucky number: 3", 10
    db "Lucky color: Purple", 10
    db 0

signs dd sign0,sign1,sign2,sign3,sign4,sign5,sign6,sign7,sign8,sign9,sign10,sign11
arts dd art0,art1,art2,art3,art4,art5,art6,art7,art8,art9,art10,art11
luckies dd lucky0,lucky1,lucky2,lucky3,lucky4,lucky5,lucky6,lucky7,lucky8,lucky9,lucky10,lucky11

month_days dd 31,28,31,30,31,30,31,31,30,31,30,31
cutoffs dd 20,19,21,20,21,21,23,23,23,23,22,22

love0 db "Capricorn, your patience may help deepen a connection today.", 10, 0
love1 db "Aquarius, your originality may help deepen a connection today.", 10, 0
love2 db "Pisces, your kindness may help deepen a connection today.", 10, 0
love3 db "Aries, your courage may help deepen a connection today.", 10, 0
love4 db "Taurus, your reliability may help deepen a connection today.", 10, 0
love5 db "Gemini, your curiosity may help deepen a connection today.", 10, 0
love6 db "Cancer, your care may help deepen a connection today.", 10, 0
love7 db "Leo, your creativity may help deepen a connection today.", 10, 0
love8 db "Virgo, your attention to detail may help deepen a connection today.", 10, 0
love9 db "Libra, your fairness may help deepen a connection today.", 10, 0
love10 db "Scorpio, your determination may help deepen a connection today.", 10, 0
love11 db "Sagittarius, your optimism may help deepen a connection today.", 10, 0

love_table dd love0,love1,love2,love3,love4,love5,love6,love7,love8,love9,love10,love11

career0 db "Capricorn, your patience may help you solve a difficult problem today.", 10, 0
career1 db "Aquarius, your originality may help you solve a difficult problem today.", 10, 0
career2 db "Pisces, your kindness may help you solve a difficult problem today.", 10, 0
career3 db "Aries, your courage may help you solve a difficult problem today.", 10, 0
career4 db "Taurus, your reliability may help you solve a difficult problem today.", 10, 0
career5 db "Gemini, your curiosity may help you solve a difficult problem today.", 10, 0
career6 db "Cancer, your care may help you solve a difficult problem today.", 10, 0
career7 db "Leo, your creativity may help you solve a difficult problem today.", 10, 0
career8 db "Virgo, your attention to detail may help you solve a difficult problem today.", 10, 0
career9 db "Libra, your fairness may help you solve a difficult problem today.", 10, 0
career10 db "Scorpio, your determination may help you solve a difficult problem today.", 10, 0
career11 db "Sagittarius, your optimism may help you solve a difficult problem today.", 10, 0

career_table dd career0,career1,career2,career3,career4,career5,career6,career7,career8,career9,career10,career11

health0 db "Capricorn, balance your patience with a peaceful break today.", 10, 0
health1 db "Aquarius, balance your originality with a peaceful break today.", 10, 0
health2 db "Pisces, balance your kindness with a peaceful break today.", 10, 0
health3 db "Aries, balance your courage with a peaceful break today.", 10, 0
health4 db "Taurus, balance your reliability with a peaceful break today.", 10, 0
health5 db "Gemini, balance your curiosity with a peaceful break today.", 10, 0
health6 db "Cancer, balance your care with a peaceful break today.", 10, 0
health7 db "Leo, balance your creativity with a peaceful break today.", 10, 0
health8 db "Virgo, balance your attention to detail with a peaceful break today.", 10, 0
health9 db "Libra, balance your fairness with a peaceful break today.", 10, 0
health10 db "Scorpio, balance your determination with a peaceful break today.", 10, 0
health11 db "Sagittarius, balance your optimism with a peaceful break today.", 10, 0

health_table dd health0,health1,health2,health3,health4,health5,health6,health7,health8,health9,health10,health11

section .bss

name resb 64
buffer resb 128
char resb 1
month resd 1
day resd 1
zodiac resd 1

section .text

global _start

_start:
    call display_welcome
    call get_user_info
    call determine_zodiac
    mov ecx, hello
    call print_string
    mov ecx, name
    call print_string
    mov ecx, bang
    call print_string
    call display_zodiac_art

.menu:
    call display_menu
    call read_number
    jc .invalid
    cmp eax, 1
    jl .invalid
    cmp eax, 6
    jg .invalid
    cmp eax, 6
    je .exit
    call show_horoscope

.return_prompt:
    mov ecx, again
    call print_string
    call read_line
    test edx, edx
    jnz .return_invalid
    cmp eax, 1
    jne .return_invalid
    mov al, [buffer]
    cmp al, 'Y'
    je .menu
    cmp al, 'y'
    je .menu
    cmp al, 'N'
    je .exit
    cmp al, 'n'
    je .exit

.return_invalid:
    mov ecx, bad_again
    call print_string
    jmp .return_prompt

.invalid:
    mov ecx, bad_menu
    call print_string
    jmp .menu

.exit:
    call exit_program

print_string:
    pushad
    mov edx, ecx

.scan:
    cmp byte [edx], 0
    je .write
    inc edx
    jmp .scan

.write:
    sub edx, ecx
    mov eax, 4
    mov ebx, 1
    int 0x80
    popad
    ret

read_line:
    push ebx
    push ecx
    push esi
    push edi
    xor esi, esi
    xor edi, edi

.next:
    mov eax, 3
    xor ebx, ebx
    mov ecx, char
    mov edx, 1
    int 0x80
    test eax, eax
    jle .eof
    mov al, [char]
    cmp al, 10
    je .done
    cmp al, 13
    je .next
    cmp esi, 127
    jae .overflow
    mov [buffer+esi], al
    inc esi
    jmp .next

.overflow:
    mov edi, 1
    jmp .next

.eof:
    test esi, esi
    jnz .done
    call exit_program

.done:
    mov byte [buffer+esi], 0
    mov eax, esi
    mov edx, edi
    pop edi
    pop esi
    pop ecx
    pop ebx
    ret

read_number:
    call read_line
    test edx, edx
    jnz .bad
    cmp eax, 1
    jl .bad
    cmp eax, 2
    jg .bad
    mov ecx, eax
    xor eax, eax
    xor esi, esi

.next:
    movzx edx, byte [buffer+esi]
    cmp edx, '0'
    jl .bad
    cmp edx, '9'
    jg .bad
    sub edx, '0'
    imul eax, eax, 10
    add eax, edx
    inc esi
    loop .next
    clc
    ret

.bad:
    stc
    ret

display_welcome:
    mov ecx, welcome
    call print_string
    ret

get_user_info:

.name:
    mov ecx, name_prompt
    call print_string
    call read_line
    test edx, edx
    jnz .bad_name
    cmp eax, 1
    jl .bad_name
    cmp eax, 63
    jg .bad_name
    xor esi, esi

.check_name:
    cmp byte [buffer+esi], ' '
    ja .copy_name
    inc esi
    cmp esi, eax
    jl .check_name

.bad_name:
    mov ecx, bad_name
    call print_string
    jmp .name

.copy_name:
    xor esi, esi

.copy:
    mov dl, [buffer+esi]
    mov [name+esi], dl
    inc esi
    test dl, dl
    jnz .copy

.month:
    mov ecx, month_prompt
    call print_string
    call read_number
    jc .bad_month
    cmp eax, 1
    jl .bad_month
    cmp eax, 12
    jg .bad_month
    mov [month], eax
    jmp .day

.bad_month:
    mov ecx, bad_month
    call print_string
    jmp .month

.day:
    mov ecx, day_prompt
    call print_string
    call read_number
    jc .bad_day
    mov [day], eax
    call validate_birthdate
    jc .bad_day
    ret

.bad_day:
    mov ecx, bad_date
    call print_string
    jmp .day

validate_birthdate:
    mov eax, [month]
    cmp eax, 1
    jl .bad
    cmp eax, 13
    jge .bad
    dec eax
    mov edx, [day]
    cmp edx, 0
    jle .bad
    cmp edx, [month_days+eax*4]
    jg .bad
    clc
    ret

.bad:
    stc
    ret

determine_zodiac:
    mov eax, [month]
    dec eax
    mov edx, [day]
    cmp edx, [cutoffs+eax*4]
    jl .store
    inc eax
    cmp eax, 12
    jne .store
    xor eax, eax

.store:
    mov [zodiac], eax
    ret

display_zodiac_art:
    mov ecx, heading
    call print_string
    mov eax, [zodiac]
    mov ecx, [arts+eax*4]
    call print_string
    mov ecx, [signs+eax*4]
    call print_string
    ret

display_menu:
    mov ecx, menu
    call print_string
    ret

show_horoscope:
    cmp eax, 1
    je .love
    cmp eax, 2
    je .career
    cmp eax, 3
    je .health
    cmp eax, 4
    je .lucky
    call display_zodiac_art
    ret

.love:
    mov ecx, love
    call print_string
    mov eax, [zodiac]
    mov ecx, [love_table+eax*4]
    jmp .print

.career:
    mov ecx, career
    call print_string
    mov eax, [zodiac]
    mov ecx, [career_table+eax*4]
    jmp .print

.health:
    mov ecx, health
    call print_string
    mov eax, [zodiac]
    mov ecx, [health_table+eax*4]
    jmp .print

.lucky:
    mov eax, [zodiac]
    mov ecx, [luckies+eax*4]

.print:
    call print_string
    ret

exit_program:
    mov ecx, bye
    call print_string
    mov eax, 1
    xor ebx, ebx
    int 0x80
```
