

##### 1. Executar <code> generate_groups_commits_and_calculate_diff({system_name})</code> para gerar os arquivos de diff de densidade entre os commits
Para rodar esse script, serão necessários os arquivos e/ou pastas:
 filepath_commits_and_parents = Caminho para o arquivo .csv que irá conter o mapeamento entre os commits e seus respectivos parents
(Default: f"data\\output\\{system_name}\\{system_name}_commits_and_parents.csv")

- folder_density_arch: Caminho para pasta onde irão estar os commits (.csv) e suas densidades de smells para cada commit
(Default: path_folder_data_collection + f"density_designite\\architecture_smells\\{system_name}\\")

- folder_smells_path: Caminho para os arquivos .csv de cada commit que irá conter os seus respectivos smells de robustez capturados com o PMD
(Default: path_folder_data_collection + f"{system_name}\\{system_name}_pmd\\")

O arquivo <code>density_data_{system}</code> será criado na pasta <code>output/{system}</code>

##### 2. Executar o método <code>generate_evolution_smells_arch({system_name})</code>

Para rodar esse script, serão necessários os arquivos e/ou pastas:
- filepath_density_data: Caminho para o arquivo .json (gerado no passo anterior) que contém a o diff de densidade entre os commits, tanto para os smells de robustez como os arquiteturais 
(Default: f"data\\output\\{system_name}\\density_data_{system_name}.json")

- filepath_commits_and_parents: Caminho para o arquivo .csv que irá conter o mapeamento entre os commits e seus respectivos parents
(Default: f"data\\output\\{system_name}\\{system_name}_commits_and_parents.csv")

<br>

O output gerado será o <code>archevolution_{system}.json</code>. Nele estará contido, para cada commit, o smell de robustez que está sendo comparado e o grupo evolutivo de cada smell arquitetural, em um período de N meses
