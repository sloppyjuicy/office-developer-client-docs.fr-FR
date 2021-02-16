---
title: Conditions préalables pour les exemples de code basés sur WCF
manager: soliver
ms.date: 09/17/2015
ms.audience: Developer
localization_priority: Normal
ms.assetid: 60d2afc8-10b6-465d-8ce8-c073da6e5054
description: Découvrez des informations pour vous aider à créer des projets dans Visual Studio à l’aide des exemples de code WCF inclus dans les rubriques de référence psi (Project Server Interface).
ms.openlocfilehash: 2222e1b3651044c41f45e57481f80093aac67bdb
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32357155"
---
# <a name="prerequisites-for-wcf-based-code-samples-in-project"></a>Conditions préalables pour les exemples de code basés sur WCF

Découvrez des informations pour vous aider à créer des projets dans Visual Studio à l’aide des exemples de code WCF inclus dans les rubriques de référence psi (Project Server Interface).
   
La plupart des exemples de code WCF inclus dans la bibliothèque de classes [project server 2013](https://msdn.microsoft.com/library/ef1830e0-3c9a-4f98-aa0a-5556c298e7d1%28Office.15%29.aspx) et la référence de service web ont été initialement créés pour la documentation du développeur Project 2010 et utilisent un format standard pour les services web WCF. Les exemples fonctionnent toujours dans Project Server 2013 et sont conçus pour être copiés dans une application console et exécutés en tant qu’unité complète. Des exceptions sont notées dans l’exemple. 
  
Les exemples de code de la documentation du développeur Project 2013 qui restent inchangés par rapport aux exemples développés pour Office Project Server 2007 utilisent les services Web ASMX. Les exemples ASMX peuvent également être adaptés pour utiliser les services WCF. Cet article montre comment utiliser les exemples avec les services WCF. Pour plus d’informations sur l’utilisation des exemples avec les services web ASMX, voir [Prerequisites for ASMX-based code samples in Project](prerequisites-for-asmx-based-code-samples-in-project.md).
  
> [!NOTE]
> Si le modèle objet côté client (CSOM) inclut les méthodes dont votre application a besoin, de nouvelles applications doivent être développées avec le modèle CSOM. Le CSOM permet aux applications de fonctionner avec Project Online ou une installation sur site de Project Server 2013. Dans le cas contraire, si votre application utilise l’interface PSI, elle doit utiliser l’interface WCF, qui est la technologie recommandée pour les communications réseau. Les applications qui utilisent l’interface ASMX ou WCF peuvent fonctionner uniquement pour les installations sur site de Project Server 2013. 
>
> Pour plus d’informations sur le modèle CSOM, voir [Project Server 2013 architecture](project-server-2013-architecture.md) and [Client-side object model (CSOM) for Project 2013](client-side-object-model-csom-for-project-2013.md). 
  
Avant d’exécutez les exemples de code, vous devez configurer l’environnement de développement, configurer l’application, ajouter un fichier de configuration de service (ou configurer les services WCF par programme) et modifier les valeurs de constante génériques en fonction de votre environnement.
  
## <a name="setting-up-the-development-environment"></a>Configuration de l'environnement de développement
<a name="pj15_PrerequisitesWCF_Setup"> </a>

1. **Configurer un système Project Server de test.**
    
    Utilisez un système Project Server de test chaque fois que vous développez ou testez. Même lorsque votre code fonctionne parfaitement, l’interprojet des dépendances, des rapports ou d’autres facteurs environnementaux peut entraîner des conséquences inattendues. 
    
    > [!NOTE]
    > Vérifiez que vous êtes un utilisateur valide sur le serveur et que vous avez les autorisations suffisantes pour les appels PSI que votre application utilise. La rubrique de documentation pour les développeurs pour chaque méthode PSI inclut une table Autorisations Project Server. Par exemple, la [méthode Project.QueueCreateProject](https://msdn.microsoft.com/library/WebSvcProject.Project.QueueCreateProject.aspx) requiert les autorisations **NewProject** globales et **SaveProjectTemplate.** 
  
    Dans certains cas, vous de devez peut-être déboguer à distance sur le serveur. Il se peut également que vous de dû configurer un programme de gestion d’événements en installant un assembly de ce dernier sur chaque ordinateur Project Server de la batterie de serveurs SharePoint, puis en configurant le handler d’événements pour l’instance Project Web App à l’aide de la page Paramètres de Project Server dans les paramètres généraux de l’application de l’Administration centrale de SharePoint.
    
2. **Configurer un ordinateur de développement.**
    
    Vous accédez généralement à l’interface PSI via un réseau. Les exemples de code sont conçus pour être exécutés sur un client distinct du serveur, sauf en cas de remarque.
    
    1. **Installez la version correcte de Visual Studio.** Sauf remarque, les exemples de code sont écrits en Visual C#. Elles peuvent être utilisées avec Visual Studio 2010 ou Visual Studio 2012. Assurez-vous que le Service Pack le plus récent est installé. 
    
    2. **Copiez les DLL Project Server sur l’ordinateur de développement.** Copiez les assemblys suivants à  `[Program Files]\Microsoft Office Servers\15.0\Bin` partir de l’ordinateur Project Server vers l’ordinateur de développement : 
    
       - Microsoft.Office.Project.Server.Events.Receivers.dll
    
       - Microsoft.Office.Project.Server.Library.dll
    
    3. Pour plus d’informations sur la compilation et l’utilisation de l’assembly de proxy ProjectServerServices.dll pour les services WCF dans l’interface PSI, voir Utilisation d’un assembly de proxy PSI et [descriptions IntelliSense données.](#pj15_PrerequisitesWCF_BuildingProxy)
    
3. **Installez les IntelliSense fichiers.**
    
    Pour utiliser des descriptions IntelliSense pour les classes et les membres dans les assemblys Project Server, copiez les fichiers XML IntelliSense mis à jour à partir du téléchargement du SDK Project 2013 dans le même répertoire que les assemblys Project Server. Par exemple, copiez le fichier Microsoft.Office.Project.Server.Library.xml dans le répertoire où votre application définira une référence à l’assembly Microsoft.Office.Project.Server.Library.dll.
    
    IntelliSense descriptions des services PSI nécessitent la création d’un assembly de proxy PSI à l’aide du script CompileWCFProxyAssembly.cmd dans le sous-dossier du téléchargement du  `Documentation\IntelliSense\WCF` SDK Project 2013. Le script crée l’assembly proxy basé sur WCF ProjectServerServices.dll proxy. Pour plus d’informations, voir le fichier [ReadMe_IntelliSense].mht dans le téléchargement du SDK. 
    
## <a name="creating-the-application-and-adding-a-service-reference"></a>Création de l’application et ajout d’une référence de service
<a name="pj15_PrerequisitesWCF_Configure"> </a>

1. **Créez une application console.**
    
    Lorsque vous créez une application console, dans  la liste de la boîte de dialogue Nouveau projet, **sélectionnez .NET Framework 4**. Vous pouvez copier l’exemple de code PSI dans la nouvelle application.
    
2. **Ajoutez les références requises pour WCF.**
    
    Dans l’Explorateur de solutions, ajoutez une référence **à System.ServiceModel** (voir figure 1). Une application web utiliserait **System.ServiceModel.Web**.
    
    Ajoutez également une référence **à System.Runtime.Serialization**.
    
    **Figure 1. Ajout des références dans Visual Studio pour une application WCF**

    ![Ajout de références pour WCF](media/pj15_PrerequisitesWCF_AddReference.gif "Ajout de références pour WCF")
  
3. **Copiez le code**.
    
    Copiez l’exemple de code complet dans Program.cs fichier de l’application console.
    
4. **Définissez l’espace de noms pour l’exemple d’application.**
    
    Vous pouvez modifier l’espace de noms répertorié en haut de l’exemple en espace de noms par défaut de l’application ou modifier l’espace de noms d’application par défaut pour qu’il corresponde à l’exemple. Vous pouvez modifier l’espace de noms d’application par défaut en modifiant les propriétés de l’application. 
    
    Par exemple, l’exemple de code [pour ReadResource](https://msdn.microsoft.com/library/WebSvcResource.Resource.ReadResource.aspx) possède l’espace de noms **Microsoft.SDK.Project.Samples.CreateResourceTest**. Si le nom du projet Visual Studio est **ResourceTest,** copiez l’espace de noms à  partir du fichier Program.cs, puis ouvrez le volet Propriétés du projet (dans le **menu** Projet, choisissez **Propriétés ResourceTest).** Sous **l’onglet Application,** copiez l’espace de noms dans la **zone de texte Espace de noms par** défaut. 
    
5. **Définissez les références de service.**
    
    De nombreux exemples nécessitent une référence à un ou plusieurs services PSI. Ceux-ci sont répertoriés dans l’exemple lui-même ou dans les commentaires qui précèdent l’exemple. Pour obtenir l’espace de noms correct des références de service, assurez-vous que vous définissez d’abord l’espace de noms d’application par défaut.
    
    Il existe trois façons d’ajouter une référence de service WCF :
    
    - Créez un assembly de proxy PSI ProjectServerServices.dll, puis définissez une référence à l’assembly. Voir [Utilisation d’un assembly de proxy PSI et IntelliSense descriptions.](#pj15_PrerequisitesWCF_BuildingProxy)
    
    - Ajoutez un fichier proxy à partir de la sortie svcutil.exe à la solution Visual Studio’accès. Voir [Ajout d’un fichier proxy PSI.](#pj15_PrerequisitesWCF_AddingProxyFile)
    
    - Ajoutez une référence de service à l’aide Visual Studio. Voir [Ajout d’une référence de service.](#pj15_PrerequisitesWCF_AddingServiceReference)
    
### <a name="using-a-psi-proxy-assembly-and-intellisense-descriptions"></a>Utilisation d’un assembly de proxy PSI et IntelliSense descriptions
<a name="pj15_PrerequisitesWCF_BuildingProxy"> </a>

Vous pouvez utiliser un assembly proxy pour tous les services WCF publics dans l’interface PSI. Compilez lProjectServerServices.dll assembly proxy à l’aide du script dans le téléchargement du  `Documentation\IntelliSense\WCF\CompileWCFProxyAssembly.cmd` SDK Project 2013, puis copiez l’assembly de proxy sur votre ordinateur de développement. Copiez ProjectServerServices.xml fichier de IntelliSense au même emplacement. Dans Visual Studio, définissez une référence à l’assembly ProjectServerServices.dll proxy. 
  
Pour les Service Packs et les mises à jour Project Server, vous pouvez mettre à jour les fichiers proxy sources et créer un assembly de proxy à l’aide du script GenWCFProxyAssembly.cmd dans le même dossier de téléchargement du SDK. Pour obtenir un lien vers le téléchargement du SDK, voir la documentation du développeur [Project 2013.](project-2013-developer-documentation.md) Pour plus d’informations, voir la section [Ajout d’une référence de service.](#pj15_PrerequisitesWCF_AddingServiceReference) 
  
> [!NOTE]
> Lorsque vous extrayez les fichiers proxy sources du fichier Source.zip, les fichiers du dossier sont à jour à la date de publication du téléchargement du  `Documentation\IntelliSense\WCF\Source` SDK Project 2013. Pour générer des fichiers sources de proxy PSI mis à jour, exécutez le script GenASMXProxyAssembly.cmd sur l’ordinateur Project Server. Pour plus d’informations, voir [Ajout d’une référence de service.](#pj15_PrerequisitesWCF_AddingServiceReference) 
> 
> Les scripts du dossier  `Documentation\IntelliSense\ASMX` ne fonctionnent pas pour les applications WCF. Le script GenASMXProxyAssembly.cmd appelle Wsdl.exe, qui génère des fichiers de code source pour les services ASMX. Les fichiers proxy ASMX incluent différentes classes et propriétés. Par exemple, le service web ressource basé sur ASMX inclut la classe **Resource,** tandis que le service de ressources WCF inclut l’interface **Resource,** l’interface **ResourceChannel** et la classe **ResourceClient.** 
  
Les espaces de noms arbitraires créés pour les services web ASMX et les services WCF sont identiques, de sorte que le fichier ProjectServerServices.xml pour IntelliSense fonctionne avec les deux assemblys. Par exemple, l’espace de noms du service ressource dans l’assembly de proxy WCF et dans l’assembly de proxy ASMX est **SvcResource**. Vous pouvez bien entendu modifier les noms des espaces de noms si vous vous assurez qu’ils correspondent dans l’assembly proxy et dans le ProjectServerServices.xml IntelliSense de noms.
  
Si un exemple de code utilise un nom différent pour un espace de noms de service PSI, par exemple **ProjectWebSvc**, pour que IntelliSense fonctionne, vous devez modifier l’exemple pour utiliser **SvcProject** afin que l’espace de noms corresponde à l’assembly de proxy. 
  
Les avantages de l’utilisation de l’assembly de proxy WCF sont les suivants :
  
- Vous pouvez développer la plupart des solutions avec l’assembly proxy sur un autre ordinateur que l’ordinateur Project Server. La définition d’une référence de service individuelle nécessite un développement sur l’ordinateur Project Server.
    
- L’assembly proxy inclut tous les espaces de noms de service PSI, vous n’avez donc pas besoin d’ajouter plusieurs fichiers proxy.
    
- Si vous ajoutez le fichier ProjectServerServices.xml au même répertoire où vous définissez une référence à l’assembly proxy ProjectServerServices.dll, vous pouvez obtenir des descriptions IntelliSense pour les classes et les membres PSI. Pour plus d’informations, voir le fichier [ReadMe_IntelliSense] dans le dossier du téléchargement du  `Documentation\IntelliSense` SDK Project 2013. 
    
**Figure 2. Utilisation IntelliSense pour une méthode dans le service de ressources**

![Utilisation d’Intellisense pour la méthode ReadResource à l’aide](media/pj15_PrerequisitesWCF_Intellisense.gif "d’Intellisense pour la méthode ReadResource")
  
Les inconvénients de l’utilisation de l’assembly de proxy sont que la solution est plus grande et que vous devez distribuer et installer l’assembly de proxy avec la solution. Vous devez également utiliser les mêmes espaces de noms que dans l’assembly proxy et les fichiers IntelliSense, sauf si vous modifiez le script pour créer un assembly de proxy et modifier le fichier ProjectServerServices.xml IntelliSense pour utiliser différents espaces de noms.
  
### <a name="adding-a-psi-proxy-file"></a>Ajout d’un fichier proxy PSI
<a name="pj15_PrerequisitesWCF_AddingProxyFile"> </a>

Le téléchargement du SDK Project 2013 inclut les fichiers sources générés par la commande SvcUtil.exe pour l’assembly proxy. Les fichiers sources sont dans le fichier Source.zip dans  `Documentation\IntelliSense\WCF` le sous-dossier. Au lieu de définir une référence à l’assembly proxy, vous pouvez ajouter un ou plusieurs des fichiers sources à une solution Visual Studio de proxy. Par exemple, pour utiliser le service Project et le service ressource, ajoutez le wcf. Project.cs et wcf. Resource.cs fichiers dans la solution. 
  
Dans WCF, la classe principale dans chaque service PSI est définie par une interface et implémentée dans une classe cliente pour l’accès aux membres. Par exemple, **l’interface SvcProject.Resource** est implémentée dans la **classe SvcProject.ResourceClient.** Pour définir un **objet ResourceClient** en tant que variable de classe **nommée resourceClient,** par exemple, utilisez le code suivant. Dans l’exemple, la méthode **SetClientEndpoints** crée un objet **resourceClient** qui utilise le point de terminaison **basicHttp_Project,** qui est défini dans le fichier app.config. Pour plus d’informations sur le app.config, voir la section [Ajout d’un](#pj15_PrerequisitesWCF_AddConfig) fichier de configuration de service. 
  
```cs
private static SvcResource.ResourceClient resourceClient;
. . .
private static void SetClientEndpoints()
{
  resourceClient = new SvcResource.ResourceClient("basicHttp_Resource");
  . . .
}
public void DisposeClients()
{
  resourceClient.Close();
  . . .
}
```

> [!NOTE]
> Que vous utilisez un assembly de proxy PSI ou que vous ajoutiez un fichier proxy pour une référence de service Project nommée **SvcResource,** vous utiliseriez le même code pour créer et éliminer un **objet resourceClient.** 
  
### <a name="adding-a-service-reference"></a>Ajout d’une référence de service
<a name="pj15_PrerequisitesWCF_AddingServiceReference"> </a>

Si vous n’utilisez pas l’assembly proxy WCF ou n’ajoutez pas de fichier proxy pour un service PSI, vous pouvez définir une ou plusieurs références de service individuelles directement dans Visual Studio. Vous pouvez également utiliser l’étape 1 de la procédure suivante pour créer des fichiers proxy mis à jour, afin de préparer le script inclus dans le téléchargement du  `Documentation\IntelliSense\WCF\GenWCFProxyAssembly.cmd` SDK Project 2013. 
  
> [!NOTE]
> Pour définir une référence de service, vous devez utiliser Visual Studio sur l’ordinateur Project Server. Nous vous recommandons d’utiliser l’assembly ProjectServerServices.dll proxy ou d’ajouter des fichiers proxy source, au lieu d’ajouter directement des références de service dans Visual Studio. 
  
Les étapes suivantes montrent comment définir une référence de service à l’aide de Visual Studio 2012 sur un ordinateur exécutant une installation de test de Project Server :
  
1. Pour accéder aux services WCF principal, exécutez Visual Studio sur l’ordinateur Project Server.
    
2. Dans **l’Explorateur de** solutions, cliquez avec le bouton droit sur le dossier **Références,** puis choisissez **Ajouter une référence de service.** 
    
3. Dans la boîte de dialogue  Ajouter une référence de **service,** dans la zone de texte Adresse, tapez https://localhost:32843/ _GUID_/psi/ServiceName .svc, puis appuyez sur **Entrée**.  Remplacez  _le GUID_ par le nom du répertoire virtuel de l’application de service Project Server, tel que 534c37eb00d74ccfadcecf9827e95239. Remplacez  _ServiceName_ par le nom du service, tel que Resource (voir figure 3). 
    
   Vous pouvez obtenir le nom du répertoire virtuel du service Project Server de l’une des manières suivantes :
    
   - Ouvrez l’application Administration centrale de SharePoint 2013 dans votre navigateur. Choisissez **Gérer les applications de service,** puis l’application de service PSI Project Server que vous souhaitez. Par exemple, choisissez **ProjectServerService**. L’URL de la page Gérer les sites Project Web App contient le nom du répertoire virtuel. Par exemple, dans , le nom du répertoire virtuel est (le nom du répertoire ne  `https://ServerName:8080/_admin/pwa/managepwa.aspx?appid=534c37eb-00d7-4ccf-adce-cf9827e95239`  `534c37eb00d74ccfadcecf9827e95239` contient pas de tirets). 
    
   - Ouvrez la boîte de dialogue Gestionnaire des **services Internet (IIS)** sur l’ordinateur Project Server. Développez le nœud Services **Web SharePoint** dans le volet Connexions, puis développez les **répertoires virtuels** de service ci-dessous, jusqu’à ce que vous trouviez le répertoire qui inclut un dossier PSI. Sélectionnez le répertoire, choisissez **Paramètres** avancés dans le volet **Actions,** puis copiez le nom du répertoire dans le **champ Chemin d’accès** virtuel. 
    
      > [!NOTE]
      > Il peut y avoir plusieurs répertoires virtuels du service Project Server. Veillez à choisir le répertoire virtuel qui contient l’instance Project Web App de votre choix. 
  
   - Utilisez **l’cmdlet get-SPServiceApplication** Windows PowerShell qui est installé avec SharePoint 2013. On the taskbar **Start** menu, choose **All Programs**, choose **Microsoft SharePoint 2013 Products**, and then choose **SharePoint 2013 Management Shell**. Voici la commande et les résultats dans la fenêtre **SharePoint 2013 Management Shell** pour les applications de service définies (vos GUI seront différents). Copiez le GUID de l’application de service Project Server. 
    
        ```powershell
            PS > get-SPServiceApplication
            DisplayName          TypeName             Id
            -----------          --------             --
            State Service        State Service        04041cfa-4ab3-4473-8bc8-3967b02eff39
            ProjectServerSer...  Project Server PS... 534c37eb-00d7-4ccf-adce-cf9827e95239
            Security Token Se... Security Token Se... 7243732e-edea-405d-8cc8-1716b99faef5
            Application Disco... Application Disco... 3bfbdeb0-bc20-4a21-801c-cc6f1ce6c643
            SharePoint Server... SharePoint Server... 09912f49-3b72-462f-a44c-6533b578286a  
        ```

      Si vous connaissez le nom complet de l’application de service Project Server, vous pouvez l’utiliser pour obtenir la valeur GUID, par exemple :
    
        ```powershell
        PS > $projectService = "ProjectServerService"
        PS > (get-SPServiceApplication -Name $projectService).Id
        Guid
        ----
        534c37eb-00d7-4ccf-adce-cf9827e95239
       ```

      > [!NOTE]
      > Supprimez les tirets du GUID pour obtenir le nom du répertoire virtuel. 
  
   Les URL, telles que  `https://localhost:32843/534c37eb00d74ccfadcecf9827e95239/PSI/Resource.svc` les services Project Server, sont standard. 
    
4. Une fois la référence de service résolue, tapez le nom de la référence dans la **zone de** texte Espace de noms. Les exemples de code de la documentation du développeur Project 2013 utilisent le nom d’espace de noms **arbitraire Svc _ServiceName_**. Par exemple, le service de ressources dans les exemples de code est nommé **SvcResource**.
    
    **Figure 3. Ajout de la référence du service de ressources basé sur WCF**

    ![Ajout de la référence de service de]ressources WCF Ajout de la référence de service de ressources basée sur(media/pj15_PrerequisitesWCF_AddSvcReference.gif "WCF")
  
5. Remplacez le fichier web.config temporaire dans le répertoire du service Project par l’original (renommé web.config), puis réexécutez  `iisreset` .
    
## <a name="setting-other-references"></a>Définition d’autres références
<a name="pj15_PrerequisitesWCF_OtherReferences"> </a>

Les applications Project Server utilisent souvent d’autres services, tels que les services web SharePoint 2013. Si d’autres services ou références sont requis, ils sont indiqués dans l’exemple de code.
  
Les références locales pour l’exemple de code sont répertoriées à **l’aide** d’instructions en haut de l’exemple. 
  
1. Dans **l’Explorateur de** solutions, cliquez avec le bouton droit sur le dossier **Références,** puis choisissez **Ajouter une référence.**
    
2. Choisissez **Parcourir,** puis accédez à l’emplacement où vous avez stocké les DLL Project Server que vous avez copiées précédemment. Choisissez les DLLs de votre choix, puis **choisissez OK.**
    
> [!NOTE]
> Assurez-vous que les versions d’assembly sur votre ordinateur de développement correspondent exactement à celles de l’ordinateur Project Server cible. 
  
## <a name="adding-a-service-configuration-file"></a>Ajout d’un fichier de configuration de service
<a name="pj15_PrerequisitesWCF_AddConfig"> </a>

Si une application configure par programme les services WCF, elle n’utilise pas de fichier de configuration de service. Dans le cas contraire, une application Windows ou une application console utilise **l’élément system.serviceModel** dans app.config fichier ; une application web **inclut system.serviceModel** dans web.config. Pour plus d’informations sur l’utilisation d’un fichier app.config ou la configuration par programme des services WCF, voir [Walkthrough: Developing PSI applications using WCF](https://msdn.microsoft.com/library/65707234-c3da-44e4-8364-32a6be28f645%28Office.15%29.aspx).
  
Lorsqu’elle génère un fichier source de proxy de service, la commande SvcUtil.exe crée également un fichier output.config qui est la base de l’élément **system.serviceModel** par défaut dans un fichier app.config ou un fichier web.config. Le téléchargement du SDK Project 2013 inclut un exemple output.config fichier dans  `Documentation\IntelliSense\WCF\Source.zip` . Par exemple, le fichier output.config par défaut créé par SvcUtil.exe service de ressources inclut deux liaisons nommées **BasicHttpBinding_Resource** et **BasicHttpBinding_Resource1**. **L’élément client** inclut deux points de terminaison par défaut. Un point de terminaison est pour l’accès sécurisé à l’adresse HTTP sur le port 32843 et l’autre pour un accès normal sur le port 32843, comme suit : 
  
```XML
<client>
    <endpoint address="https://ServerName.domain:32843/GUID/PSI/Resource.svc/secure"
        binding="basicHttpBinding" bindingConfiguration="BasicHttpBinding_Resource"
        contract="SvcResource.Resource" name="BasicHttpBinding_Resource" />
address="https://ServerName.domain:32843/GUID/PSI/Resource.svc"
        binding="basicHttpBinding" bindingConfiguration="BasicHttpBinding_Resource1"
        contract="SvcResource.Resource" name="BasicHttpBinding_Resource1" />
</client>
```

La configuration du service PSI n’utilise pas les liaisons et points de terminaison par défaut. Project Server exige que les applications accèdent aux services PSI par le biais de ProjectServer.svc frontal, qui agit en tant que routeur pour les appels aux services frontaux. Pour créer le fichier app.config, faites les étapes suivantes :
  
1. Si vous définissez une référence à l’assembly de proxy ProjectServerServices.dll ou ajoutez le fichier proxy source d’un service, l’application ne contient pas de app.config fichier. Ajoutez un nouvel élément au Visual Studio projet. Dans la **boîte de dialogue Ajouter un nouvel** élément, choisissez le modèle de fichier de configuration de l’application, nommez-le app.config, puis choisissez **Ajouter**. 
    
2. Supprimez tout le texte app.config fichier, puis copiez le code suivant dans le fichier. Vous pouvez utiliser la même liaison, par exemple, pour chaque point de  `basicHttpConf` terminaison de service. Si vous souhaitez utiliser plusieurs liaisons, par exemple, pour lier des protocoles HTTP et HTTPS, vous devez créer une liaison pour chaque protocole.
    
    ```XML
        <?xml version="1.0" encoding="utf-8" ?>
        <configuration>
            <system.serviceModel>
                <behaviors>
                    <endpointBehaviors>
                        <behavior name="basicHttpBehavior">
                            <clientCredentials>
                                <windows allowedImpersonationLevel="Impersonation" />
                            </clientCredentials>
                        </behavior>
                    </endpointBehaviors>
                </behaviors>
                <bindings>
                    <basicHttpBinding>
                        <binding name="basicHttpConf" sendTimeout="01:00:00" 
                            maxBufferSize="500000000" maxReceivedMessageSize="500000000">
                            <readerQuotas maxDepth="32" maxStringContentLength="8192" 
                                maxArrayLength="16384" maxBytesPerRead="4096" 
                                maxNameTableCharCount="500000000" />
                            <security mode="TransportCredentialOnly">
                                <transport clientCredentialType="Ntlm" realm="https://SecurityDomain" />
                            </security>
                        </binding>
                    </basicHttpBinding>
                </bindings>
                <client>
                    <endpoint address="https://ServerName/ProjectServerName/_vti_bin/PSI/ProjectServer.svc"
                        behaviorConfiguration="basicHttpBehavior" binding="basicHttpBinding"
                        bindingConfiguration="basicHttpConf" 
                        contract="SvcServiceName.ServiceName"
                        name="basicHttp_ServiceName" />
                </client>
            </system.serviceModel>
        </configuration>
    ```

3. Remplacez  `ServerName/ProjectServerName` l’adresse du point de terminaison client par le nom de votre serveur et de l’instance Project Web App. 
    
4. Remplacez  `ServiceName` par le nom du service PSI, tel que Resource. Veillez à remplacer les trois instances du nom du service, par exemple :
    
    ```XML
        <endpoint address="https://myserver/pwa/_vti_bin/PSI/ProjectServer.svc"
            behaviorConfiguration="basicHttpBehavior" binding="basicHttpBinding"
            bindingConfiguration="basicHttpConf" 
            contract="SvcResource.Resource"
            name="basicHttp_Resource" />
    ```

5. Pour utiliser plusieurs services PSI, créez un élément **de** point de terminaison pour chaque service et pour chaque élément **de** liaison utilisé par le service. Par exemple, les points de terminaison suivants configurent le client pour utiliser la liaison HTTP de base pour le service Project et le service QueueSystem. 
    
    > [!NOTE]
    > Si vous exécutez une application et que vous obtenez une erreur qui vous dit que le serveur est trop occupé ou que la demande HTTP n’est pas autorisée, assurez-vous que les adresses de point de terminaison sont correctes dans le fichier app.config. 
  
    ```XML
        <client>
        <endpoint address="https://ServerName/pwa/_vti_bin/PSI/ProjectServer.svc"
            behaviorConfiguration="basicHttpBehavior" binding="basicHttpBinding"
            bindingConfiguration="basicHttpConf" 
            contract="SvcProject.Project"
            name="basicHttp_Project" />
        <endpoint address="https://ServerName/pwa/_vti_bin/PSI/ProjectServer.svc"
            behaviorConfiguration="basicHttpBehavior" binding="basicHttpBinding"
            bindingConfiguration="basicHttpConf" 
            contract="SvcQueueSystem.QueueSystem"
            name="basicHttp_QueueSystem" />
        </client>
    ```

Vous pouvez modifier un fichier app.config à l’aide de l’Éditeur de configuration de **service WCF** Visual Studio (dans le menu **Outils).** La figure 4 montre comment définir l’élément **contract** dans la boîte de dialogue **Microsoft Service Configuration Editor.** Si la solution utilise l’assembly de proxy PSI, ProjectServerServices.dll dans le répertoire  `bin\debug` de la solution Visual Studio. La **boîte de dialogue Explorateur de types** de contrat affiche tous les contrats de service WCF (voir figure 5). 
  
**Figure 4. Utilisation de l’éditeur de configuration de service WCF**

![Utilisation de l’éditeur de configuration]de service WCF(media/pj15_PrerequisitesWCF_ServiceConfigurationEditor.gif "à l’aide de l’éditeur de configuration de service WCF")
  
Si la solution utilise un fichier proxy de service, tel que wcfResource.cs, compilez l’application, puis ouvrez le fichier exécutable dans  `bin\debug` le répertoire. Pour plus d’informations sur la modification du fichier app.config, voir [Walkthrough: Developing PSI applications using WCF](https://msdn.microsoft.com/library/65707234-c3da-44e4-8364-32a6be28f645%28Office.15%29.aspx).
  
**Figure 5. Utilisation de l’explorateur de types de contrat dans l’éditeur de configuration du service WCF**

![Utilisation de l’explorateur de types de contrat]à(media/pj15_PrerequisitesWCF_ContractTypeBrowser.gif "l’aide de l’explorateur de types de contrat")
  
## <a name="using-multiple-authentication"></a>Utilisation de l’authentification multiple
<a name="pj15_PrerequisitesWCF_ClaimsMultiAuth"> </a>

L’authentification des utilisateurs Project Server locaux, que ce soit par l’authentification Windows ou par l’authentification par formulaires, est effectuée par le biais du traitement des revendications dans SharePoint. L’authentification multiple signifie que l’application web sur laquelle Project Web App est provisioné prend en charge l’authentification Windows et l’authentification basée sur les formulaires. Si tel est le cas, tout appel à un service WCF qui utilise l’authentification Windows échouera avec l’erreur suivante, car le processus de revendications ne peut pas déterminer le type d’utilisateur à authentifier :
  
`The server was unable to process the request due to an internal error. For more information about the error, either turn on Include ExceptionDetailInFaults (either from ServiceBehaviorAttribute or from the <serviceDebug> configuration behavior) on the server in order to send the exception information back to the client, or turn on tracing as per the Microsoft .NET Framework 3.0 SDK documentation and inspect the server trace logs.`

Pour résoudre le problème de WCF, tous les appels aux méthodes PSI doivent se trouver dans un **OperationContextScope** défini pour chaque service PSI. N’imbriez pas d’étendues pour plusieurs services ; par exemple, lorsque vous utilisez des appels aux services Ressource et Projet, chaque ensemble d’appels doit se trouver dans sa propre portée. 
  
Dans l’exemple suivant, la **méthode DisableFormsAuth** peut être appelée à partir de chaque section **OperationContextScope** d’une application. La méthode supprime toute valeur d’en-tête qui désactivait précédemment l’authentification par formulaires, afin que l’authentification par formulaires puisse continuer si le paramètre  _isWindowsAuth_ est **false**. Si  _isWindowsAuth_ est **vrai,** la **méthode DisableFormsAuth** désactive l’authentification par formulaires. 
  
Dans la **méthode WcfSample,** l’objet **projectClient** est une instance de la classe PSI **SvcProject.ProjectClient.** 
  
```cs
// Class variable that determines whether to disable Forms authentication.
private bool isWindowsUser = true;
public void DisableFormsAuth(bool isWindowsAuth)
{
    WebOperationContext.Current.OutgoingRequest.Headers.Remove(
        "X-FORMS_BASED_AUTH_ACCEPTED");
    if (isWindowsAuth)
    {
        // Disable Forms authentication, to enable Windows authentication.
        WebOperationContext.Current.OutgoingRequest.Headers.Add(
            "X-FORMS_BASED_AUTH_ACCEPTED", "f");
    }
}
private void WcfSample()
{
    // Limit the scope of WCF calls to the client channel. 
    using (OperationContextScope scope = new OperationContextScope(projectClient.InnerChannel))
    {
        // Add a web request header to enable Windows authentication in 
        // multiple authentication installations.
        DisableFormsAuth(isWindowsUser);
        // Add calls to the projectClient methods here:
        // . . .
    }
}
```

> [!NOTE]
> La réalisation d’appels PSI dans **un OperationContextScope** est requise uniquement pour les applications qui s’exécutent dans un environnement d’authentification multiple. Si Project Server utilise uniquement l’authentification Windows, il n’est pas nécessaire de définir une étendue et d’ajouter un en-tête de demande web qui désactive l’authentification par formulaires. 
> 
> Le correctif d’une application ASMX est différent. Pour plus d’informations, voir la section Utilisation de l’authentification  *multiple*  dans [Prerequisites for ASMX-based code samples in Project](prerequisites-for-asmx-based-code-samples-in-project.md). 
  
## <a name="changing-values-of-generic-constants"></a>Modification des valeurs des constantes génériques
<a name="pj15_PrerequisitesWCF_ChangeValues"> </a>

La plupart des exemples ont une ou plusieurs variables que vous devez mettre à jour pour que l’exemple fonctionne correctement dans votre environnement. Dans l’exemple suivant, si SSL est installé, utilisez le protocole HTTPS au lieu du protocole HTTP. Remplacez  _ServerName_ par le nom du serveur que vous utilisez. Remplacez  _ProjectServerName_ par le nom du répertoire virtuel de votre site de serveur de projet, tel que PWA. 
  
```cs
const string PROJECT_SERVER_URI = "https://ServerName/ProjectServerName/";
```

Toutes les autres variables que vous devez modifier sont notées en haut de l’exemple de code.
  
## <a name="verifying-the-results"></a>Vérification des résultats
<a name="pj15_PrerequisitesWCF_Verify"> </a>

L’obtention et l’interprétation des résultats à partir d’un exemple de code ne sont pas toujours simples. Par exemple, si vous créez un projet, vous devez le publier pour qu’il puisse apparaître dans la page Centre de projets dans Project Web App.
  
Vous pouvez vérifier les résultats des exemples de code de plusieurs manières, par exemple :
  
- Utilisez le client Project Professionnel 2013 pour ouvrir le projet à partir de l’ordinateur Project Server et afficher les éléments que vous souhaitez.
    
- Afficher les projets publiés dans la page Centre de projets de Project Web App ( `https://ServerName/ProjectServerName/projects.aspx` ).
    
- Afficher le journal de file d’attente dans Project Web App. Ouvrez la page Paramètres du serveur (sélectionnez l’icône  **Paramètres** dans le coin supérieur droit), puis choisissez Mes travaux en file d’attente sous la section **Paramètres** personnels ( `https://ServerName/ProjectServerName/MyJobs.aspx` ). Dans la **liste de** listes, vous pouvez trier en fonction de l’état du travail. L’état par défaut **est En cours et Travaux en échec de la semaine dernière.** 
    
- Utilisez la page Paramètres du serveur dans Project Web App ( ) pour gérer tous les travaux en file d’attente et supprimer ou forcer l’enregistrement des objets `https://ServerName/ProjectServerName/_layouts/15/pwa/admin/admin.aspx` d’entreprise. Vous devez avoir des autorisations administratives pour accéder à ces liens dans la page Paramètres du serveur.
    
- Utilisez **Microsoft SQL Server Management Studio** pour exécuter une requête sur une table d’une base de données Project Server. Par exemple, utilisez la requête suivante pour sélectionner les 200 premières lignes du tableau MSP_WORKFLOW_STAGE_PDPS afin d’afficher des informations sur les pages de détails de projet (PDP) par étapes de flux de travail. 
    
```sql
        SELECT TOP 200 [STAGE_UID]
                ,[PDP_UID]
                ,[PDP_NAME]
                ,[PDP_POSITION]
                ,[PDP_ID]
                ,[PDP_STAGE_DESCRIPTION]
                ,[PDP_REQUIRES_ATTENTION]
        FROM [ProjectService].[pub].[MSP_WORKFLOW_STAGE_PDPS]
```

## <a name="cleaning-up"></a>Nettoyage
<a name="pj15_PrerequisitesWCF_Cleanup"> </a>

Après avoir testé certains exemples de code, certains objets et paramètres d’entreprise doivent être supprimés ou réinitialisés. Vous pouvez utiliser la page Paramètres du serveur dans Project Web App pour gérer les données d’entreprise ( `https://ServerName/ProjectServerName/_layouts/15/pwa/admin/admin.aspx` ). Les liens de la page Paramètres du serveur vous permettent de supprimer les anciens éléments, de forcer l’enregistrement des projets, de gérer la file d’attente des travaux pour tous les utilisateurs et d’effectuer d’autres tâches administratives.
  
Voici quelques liens sur la page Paramètres du serveur à utiliser pour les activités de nettoyage classiques après l’exécution d’exemples de code :
  
- **Champs personnalisés d’entreprise et tables de choix**
    
- **Gérer les travaux en file d’attente**
    
- **Supprimer des objets d’entreprise**
    
- **Forcer l’enregistrement des objets d’entreprise**
    
- **Types de projets d’entreprise**
    
- **Phases du flux de travail**
    
- **Étapes du flux de travail**
    
- **Pages de détails de projet**
    
- **Périodes de rapports de temps**
    
- **Paramètres et valeurs par défaut de la feuille de temps**
    
- **Classifications des lignes**
    
Les paramètres supplémentaires sont gérés par SharePoint Server 2013 pour chaque instance de Project Web App, plutôt que par une page de paramètres de serveur Project Web App spécifique. Dans l’application Administration centrale de SharePoint,  choisissez **Paramètres** généraux de l’application, gérer sous **Paramètres de Project Server,** puis sélectionnez l’instance Project Web App dans la liste de listes dans la page Paramètres du serveur. Par exemple, choisissez **les** gestions d’événements côté serveur pour ajouter ou supprimer des handlers d’événements pour l’instance Project Web App sélectionnée. 
  
## <a name="see-also"></a>Voir aussi

- [Conditions préalables pour les exemples de code basés sur ASMX](prerequisites-for-asmx-based-code-samples-in-project.md)   
- [Walkthrough: Developing PSI applications using WCF](https://msdn.microsoft.com/library/65707234-c3da-44e4-8364-32a6be28f645%28Office.15%29.aspx)   
- [Utiliser l’emprunt d’identité avec WCF](https://msdn.microsoft.com/library/e3597901-2f02-44a2-8076-d32aae540b38%28Office.15%29.aspx)  
- [Vue d’ensemble de la référence Project PSI](project-psi-reference-overview.md) 
- [Centre de développement SharePoint](https://msdn.microsoft.com/sharepoint/default.aspx)
    

