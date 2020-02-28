ConfigrableApplicationContext context = SpringbootApplication.run(App.class, args);  
SpringApplication app = new SpringApplication();
app.setSources(app.class);
ConfigrableApplicationContext context = app.run(args);
