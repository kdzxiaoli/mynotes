@SprintBootTest(properties=value, webenviroment=???????)
EnviromentTestUtils.addEnviroment


@MockBean
private userMapper usermapper;
BDDMokito.given().willReturn()


@Test(expected=NullPointerException.class)


@TestRestTemplate template test controller

template.getForObject("/user", String.class)


@WebMvcTest(controller=?????) replace SprintBootTest 不会加载spring容器   依赖会报错 如果需要加载all  
需要用@springboottest && @AutoConfigureWebMvc



@Autowired
private MockMvc mvc

mvc.perform(MockMvcRequestBuilder.get("/dfdf").param(...).andExpect(MockMvcResultMatchers.status().isOk()).and......content)
