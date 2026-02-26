# Provisioners





## Always run the provisioner (1.6+)



```ruby
config.vm.provision "shell", run: "always" do |s|
  s.inline = "echo hello"
end
```

