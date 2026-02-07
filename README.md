stack_menu.py
from collections import deque

# Nama pembuat
nama_pembuat = "Iche Wanenda"

stack = deque()

while True:
    print("\n=== PROGRAM STACK ===")
    print("a. Append")
    print("b. Append Left")
    print("c. Pop")
    print("d. Pop Left")
    print("e. Clear")
    print("f. Keluar")

    pilihan = input("Pilih menu (a-f): ").lower()

    if pilihan == "a":
        data = input("Masukkan data: ")
        stack.append(data)
        print("Stack:", list(stack))

    elif pilihan == "b":
        data = input("Masukkan data: ")
        stack.appendleft(data)
        print("Stack:", list(stack))

    elif pilihan == "c":
        if stack:
            print("Data yang dihapus:", stack.pop())
        else:
            print("Stack kosong!")
        print("Stack:", list(stack))

    elif pilihan == "d":
        if stack:
            print("Data yang dihapus:", stack.popleft())
        else:
            print("Stack kosong!")
        print("Stack:", list(stack))

    elif pilihan == "e":
        stack.clear()
        print("Stack telah dikosongkan!")

    elif pilihan == "f":
        print("Program selesai.")
        break

    else:
        print("Pilihan tidak valid!")
