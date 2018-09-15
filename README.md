# Usage

This module provides a maven version rule set to ignore certain releases
from update suggestions.  By cutting down this noise it's easier to see
updates of value.


Use by including the following in your maven plugin definition

      <plugin>
        <groupId>org.codehaus.mojo</groupId>
        <artifactId>versions-maven-plugin</artifactId>
        <version>2.7</version>
        <configuration>
          <rulesUri>classpath:///com/purplepip/maven/version/maven-version-rules.xml</rulesUri>
        </configuration>
        <dependencies>
          <dependency>
            <groupId>com.purplepip</groupId>
            <artifactId>maven-version-rules</artifactId>
            <version>1.0</version>
          </dependency>
        </dependencies>
      </plugin>