gg.alert("Anger of Stick 5 Cheat Activated!")

function main()
  menu = gg.multiChoice({
    "1. Unlimited Money",
    "2. Unlimited Health",
    "3. Unlock All Characters",
    "4. High Damage",
    "5. Speed Hack",
    "6. Exit"
  }, nil, "Select Cheat to Activate")

  if menu == nil then
    -- Do nothing
  else
    if menu[1] then money() end
    if menu[2] then health() end
    if menu[3] then unlock() end
    if menu[4] then damage() end
    if menu[5] then speed() end
    if menu[6] then exit() end
  end
end

function money()
  gg.searchNumber("9999", gg.TYPE_DWORD) -- contoh nilai uang
  gg.getResults(100)
  gg.editAll("99999999", gg.TYPE_DWORD)
  gg.toast("Unlimited Money Activated!")
end

function health()
  gg.searchNumber("100", gg.TYPE_FLOAT) -- contoh darah normal
  gg.getResults(100)
  gg.editAll("99999", gg.TYPE_FLOAT)
  gg.toast("Unlimited Health Activated!")
end

function unlock()
  gg.searchNumber("0", gg.TYPE_DWORD) -- terkunci (locked = 0)
  gg.getResults(100)
  gg.editAll("1", gg.TYPE_DWORD) -- unlock = 1
  gg.toast("All Characters Unlocked!")
end

function damage()
  gg.searchNumber("10", gg.TYPE_FLOAT) -- normal damage
  gg.getResults(100)
  gg.editAll("9999", gg.TYPE_FLOAT)
  gg.toast("High Damage Activated!")
end

function speed()
  gg.setSpeed(3.0) -- Speed Hack 3x
  gg.toast("Speed Hack Activated!")
end

function exit()
  gg.toast("Exiting Cheat...")
  os.exit()
end

while true do
  if gg.isVisible(true) then
    gg.setVisible(false)
    main()
  end
end
