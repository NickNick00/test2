
local Window = Fluent:CreateWindow({
    Title = "Kyuzzy " .. Fluent.Version,
    TabWidth = 160, Size = UDim2.fromOffset(580, 460), Theme = "Dark"
})

local Tabs = {
    Main = Window:AddTab({ Title = "principal" }),
    Settings = Window:AddTab({ Title = "config", Icon = "settings" })
}

Fluent:Notify({ Title = "Notific", Content = "This is a notification" })


Tabs.Main:AddParagraph({ Title = "teste1", Content = "This is a paragraph.\nSecond line!" })


Tabs.Main:AddButton({ Title = "kyus", Callback = function() ... end })

local Toggle = Tabs.Main:AddToggle("MyToggle", { Title = "Toggle" })
Toggle:OnChanged(function() print(Options.MyToggle.Value) end)

Window:SelectTab(1)
Fluent:Notify({ Title = "Fluent", Content = "The script has been loaded." })
