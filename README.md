gg.alert("Script Slot GG by ChatGPT - Edukasi")
gg.setVisible(false)

function main()
  gg.clearResults()
  gg.searchNumber("1000", gg.TYPE_DWORD) -- Ganti 1000 dengan jumlah koin kamu
  gg.refineNumber("1000", gg.TYPE_DWORD)
  local results = gg.getResults(1)
  if #results == 0 then
    gg.alert("Nilai tidak ditemukan!")
  else
    gg.editAll("999999", gg.TYPE_DWORD) -- Ganti ke jumlah koin yang diinginkan
    gg.toast("Koin berhasil diubah!")
  end
end

main()
