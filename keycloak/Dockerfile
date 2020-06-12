FROM jboss/keycloak:4.6.0.Final

WORKDIR /opt/jboss/keycloak

COPY realm-export.json /opt/jboss/keycloak/

EXPOSE 8443

ENTRYPOINT [ "/opt/jboss/tools/docker-entrypoint.sh" ]
CMD ["-b", "0.0.0.0", "-bmanagement", "0.0.0.0", "-Dkeycloak.import=realm-export.json -Dkeycloak.migration.strategy=OVERWRITE_EXISTING"]

