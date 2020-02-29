add actuator dependent

implement HealthyIndicator


/info 为空  
可在properties info.name  info.age   etc

CounterService 访问状态计数  

GaugeService 设置值

打印到JDK view

@Bean
@ExportMetricWriter
public MetricWriter createMetricWriter(MBeanExporter exporter) {
	return new JmxMetricWriter(exporter)
}
