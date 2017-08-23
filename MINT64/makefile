all: BootLoader Disk.img LunchBootLoader


BootLoader:
	@echo
	@echo ======================== Build Boot Loader ========================
	@echo
	make -C 00.BootLoader
	@echo
	@echo ========================= Build Complete =========================
	@echo


Disk.img: 00.BootLoader/BootLoader.bin
	@echo
	@echo ===================== Disk Image Build Start =====================
	@echo
	cp 00.BootLoader/BootLoader.bin Disk.img
	@echo
	@echo ======================= All Build Complete =======================
	@echo

LunchBootLoader:
	@echo
	@qemu-system-x86_64 -m 64 -fda ./Disk.img -localtime -M pc
	@echo

clean:
	make -C 00.BootLoader clean
	rm -f Disk.img
