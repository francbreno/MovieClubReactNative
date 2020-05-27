default_platform(:android)

platform :ios do
  desc "Build para TestFlight"
  lane :tests do
    UI.header "Iniciando build de testes para TestFlight na Apple Store"
  end

  desc "Build para App Store"
  lane :store do
    UI.header "Iniciando build de produção para Apple Store"
  end
end

platform :android do
  desc "Build para Play Tests"
  lane :beta do
    UI.header "Iniciando build de testes para Play Store"
    
    gradle(task: "clean assemble")
    upload_to_play_store(track: 'beta')

    UI.success "Build realizado com sucesso! App disponível para testes na Play Store"
  end

  desc "Build para Google Play Store"
  lane :store do
    UI.header "Iniciando build de produção para Play Store"

    gradle(task: "clean assemble")

    UI.success "Build realizado com sucesso! App disponível na Play Store"
  end
end