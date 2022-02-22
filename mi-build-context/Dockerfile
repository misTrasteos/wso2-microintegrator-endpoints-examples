FROM wso2/wso2mi:4.0.0

WORKDIR ${WSO2_SERVER_HOME}

RUN mkdir registry

COPY --chown=wso2carbon:wso2 apis repository/deployment/server/synapse-configs/default/api
