---
title: Conditions préalables pour les exemples de code basée sur WCF dans Project
manager: soliver
ms.date: 09/17/2015
ms.audience: Developer
localization_priority: Normal
ms.assetid: 60d2afc8-10b6-465d-8ce8-c073da6e5054
description: Découvrez des informations pour vous aider à créer des projets dans Visual Studio en utilisant les exemples de code basée sur WCF qui sont inclus dans les rubriques de référence d’Interface de Project Server (PSI).
ms.openlocfilehash: 43700a9db4445dacf366c7ca2efe1bfb10914372
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19787932"
---
# <a name="prerequisites-for-wcf-based-code-samples-in-project"></a>Conditions préalables pour les exemples de code basée sur WCF dans Project

Découvrez des informations pour vous aider à créer des projets dans Visual Studio en utilisant les exemples de code basée sur WCF qui sont inclus dans les rubriques de référence d’Interface de Project Server (PSI).
   
De nombreux exemples de code basée sur WCF inclus dans la [référence de classe Project Server 2013 service web et de bibliothèque](http://msdn.microsoft.com/library/ef1830e0-3c9a-4f98-aa0a-5556c298e7d1%28Office.15%29.aspx) ont été créés pour la documentation du développeur Project 2010 et utilisent un format standard pour les services web WCF. Les exemples de toujours utiliser dans Project Server 2013 et sont conçus pour être copiés dans une application de console et exécuter en tant qu’une unité complète. Exceptions sont indiquées dans l’exemple. 
  
Dans la documentation du développeur Project 2013, des exemples de code qui ne sont pas modifiées dans les exemples de développé pour Office Project Server 2007 utilisent les services Web ASMX. Les exemples de basées sur ASMX peuvent également être adaptées pour utiliser les services WCF. Cet article explique comment utiliser les exemples avec les services WCF. Pour plus d’informations sur la façon d’utiliser les exemples avec des services web ASMX, voir [conditions préalables pour les exemples de code basées sur ASMX dans Project](prerequisites-for-asmx-based-code-samples-in-project.md).
  
> [!NOTE]
> Si le modèle objet côté client (CSOM) comprend les méthodes requis par votre application, les nouvelles applications doivent être développées avec le modèle CSOM. Le modèle CSOM permet aux applications fonctionner avec Project Online ou une installation locale de Project Server 2013. Sinon, si votre application utilise l’interface PSI, elle doit utiliser l’interface WCF, qui est la technologie que nous recommandons pour les communications réseau. Applications qui utilisent l’interface ASMX ou WCF peuvent fonctionner uniquement pour les installations locales de Project Server 2013. 
>
> Pour plus d’informations sur le modèle CSOM, voir [architecture de Project Server 2013](project-server-2013-architecture.md) et [modèle d’objet côté Client (CSOM) pour Project 2013](client-side-object-model-csom-for-project-2013.md). 
  
Avant d’exécuter les exemples de code, vous devez définir l’environnement de développement, configurer l’application, ajoutez un fichier de configuration de service (ou configurer les services WCF par programme) et modifier les valeurs de constante génériques correspondant à votre environnement.
  
## <a name="setting-up-the-development-environment"></a>Configuration de l'environnement de développement
<a name="pj15_PrerequisitesWCF_Setup"> </a>

1. **Configurer un système de Project Server de test.**
    
    Utilisez un test système Project Server lorsque vous développez ou de test. Même lorsque votre code fonctionne parfaitement, dépendances interprojets, création de rapports ou d’autres facteurs environnementaux peuvent entraîner des conséquences inattendues. 
    
    > [!NOTE]
    > Assurez-vous que vous êtes un utilisateur valide sur le serveur et vérifiez que vous disposez des autorisations suffisantes pour les appels PSI par votre application. La rubrique de la documentation du développeur pour chaque méthode PSI comprend un tableau d’autorisations Project Server. Par exemple, la méthode [Project.QueueCreateProject](https://msdn.microsoft.com/library/WebSvcProject.Project.QueueCreateProject.aspx) nécessite l’autorisation **NewProject** globale et l’autorisation **SaveProjectTemplate** . 
  
    Dans certains cas, vous devrez effectuer un débogage distant sur le serveur. Vous devrez également configurer un gestionnaire d’événements à l’installation d’un assembly du Gestionnaire d’événements sur chaque ordinateur de Project Server dans la batterie de serveurs SharePoint, puis configurer le Gestionnaire d’événements pour l’instance Project Web App à l’aide de la page Paramètres de Project Server général Paramètres de l’application de l’Administration centrale de SharePoint.
    
2. **Configurer un ordinateur de développement.**
    
    Vous accédez généralement la PSI via un réseau. Les exemples de code sont conçus pour être exécutée sur un client qui est différent du serveur, sauf indication contraire.
    
    1. **Installer la version appropriée de Visual Studio.** Sauf mention contraire, les exemples de code sont écrits en Visual c#. Ils peuvent être utilisés avec Visual Studio 2010 ou Visual Studio 2012. Assurez-vous d’avoir le service pack le plus récent. 
    
    2. **Copiez la DLL de Project Server sur l’ordinateur de développement.** Copiez les assemblys suivants à partir de `[Program Files]\Microsoft Office Servers\15.0\Bin` sur l’ordinateur Project Server sur l’ordinateur de développement : 
    
       - Microsoft.Office.Project.Server.Events.Receivers.dll
    
       - Microsoft.Office.Project.Server.Library.dll
    
    3. Pour plus d’informations sur la compilation et l’utilisation de l’assembly de proxy ProjectServerServices.dll pour les services WCF dans l’interface PSI, voir [l’aide d’un assembly de proxy PSI et descriptions IntelliSense](#pj15_PrerequisitesWCF_BuildingProxy).
    
3. **Installez les fichiers IntelliSense.**
    
    Pour utiliser les descriptions IntelliSense pour les classes et membres dans les assemblys de Project Server, copie les fichiers XML IntelliSense mis à jour à partir du Kit de développement Project 2013 téléchargement dans le même répertoire où se trouvent les assemblys de Project Server. Par exemple, copiez le fichier Microsoft.Office.Project.Server.Library.xml dans le répertoire où votre application sera défini une référence à l’assembly Microsoft.Office.Project.Server.Library.dll.
    
    Les descriptions IntelliSense pour les services PSI requièrent la création d’un assembly de proxy PSI à l’aide du script CompileWCFProxyAssembly.cmd dans les `Documentation\IntelliSense\WCF` sous-répertoire dans le téléchargement du Kit de développement Project 2013. Le script crée l’assembly de proxy ProjectServerServices.dll basée sur WCF. Pour plus d’informations, consultez le fichier .mht [ReadMe_IntelliSense] du téléchargement SDK. 
    
## <a name="creating-the-application-and-adding-a-service-reference"></a>Création de l’application et en ajoutant une référence de service
<a name="pj15_PrerequisitesWCF_Configure"> </a>

1. **Créer une application console.**
    
    Lorsque vous créez une application console, dans la liste déroulante de la boîte de dialogue **Nouveau projet** , sélectionnez **.NET Framework 4**. Vous pouvez copier le code d’exemple PSI dans la nouvelle application.
    
2. **Ajoutez les références requises pour WCF.**
    
    Dans l’Explorateur de solutions, ajoutez une référence à **System.ServiceModel** (voir Figure 1). Une application web utilise **System.ServiceModel.Web**.
    
    Également ajouter une référence à **System.Runtime.Serialization**.
    
    **La figure 1. Ajout des références dans Visual Studio pour une application basée sur WCF**

    ![Ajout de références pour WCF] (media/pj15_PrerequisitesWCF_AddReference.gif "Ajout de références pour WCF")
  
3. **Copiez le code**.
    
    Copiez l’exemple de code complet dans le fichier Program.cs de l’application console.
    
4. **Définir l’espace de noms pour l’exemple d’application.**
    
    Vous pouvez modifier l’espace de noms répertorié dans la partie supérieure de l’échantillon à l’espace de noms par défaut application, ou modifier l’espace de noms par défaut application correspondant à l’exemple. Vous pouvez modifier l’espace de noms par défaut application en modifiant les propriétés de l’application. 
    
    Par exemple, l’exemple de code pour [ReadResource](https://msdn.microsoft.com/library/WebSvcResource.Resource.ReadResource.aspx) a l’espace de noms **Microsoft.SDK.Project.Samples.CreateResourceTest**. Si le nom du projet Visual Studio est **ResourceTest**, copiez l’espace de noms à partir du fichier Program.cs et puis ouvrez le volet de **Propriétés** de projet (dans le menu **projet** , choisissez **Propriétés ResourceTest**). Sous l’onglet **Application** , copiez l’espace de noms dans la zone de texte **par défaut d’espace de noms** . 
    
5. **Définir les références de service.**
    
    De nombreux exemples requièrent une référence à une ou plusieurs des services PSI. Ils sont répertoriés dans l’exemple lui-même ou dans des commentaires qui précèdent l’échantillon. Pour obtenir l’espace de noms correct des références de service, vérifiez que tout d’abord définir l’espace de noms par défaut application.
    
    Il existe trois façons d’ajouter une référence de service WCF :
    
    - Créer un assembly de proxy PSI nommé ProjectServerServices.dll, puis définir une référence à l’assembly. Consultez [l’aide d’un assembly de proxy PSI et descriptions IntelliSense](#pj15_PrerequisitesWCF_BuildingProxy).
    
    - Ajoutez un fichier de proxy à partir de la sortie de svcutil.exe à la solution Visual Studio. Consultez la rubrique [Ajout d’un fichier de proxy PSI](#pj15_PrerequisitesWCF_AddingProxyFile).
    
    - Ajoutez une référence de service à l’aide de Visual Studio. Consultez [Ajout d’une référence de service](#pj15_PrerequisitesWCF_AddingServiceReference).
    
### <a name="using-a-psi-proxy-assembly-and-intellisense-descriptions"></a>À l’aide d’un assembly de proxy PSI et descriptions IntelliSense
<a name="pj15_PrerequisitesWCF_BuildingProxy"> </a>

Vous pouvez utiliser un assembly de proxy pour tous les services WCF publics dans l’interface PSI. Compiler l’assembly de proxy ProjectServerServices.dll à l’aide de la `Documentation\IntelliSense\WCF\CompileWCFProxyAssembly.cmd` de script dans le téléchargement du Kit de développement Project 2013, puis copiez l’assembly de proxy sur votre ordinateur de développement. Copiez le fichier ProjectServerServices.xml pour IntelliSense au même emplacement. Dans Visual Studio, définissez une référence à l’assembly de proxy ProjectServerServices.dll. 
  
Pour Project Server service packs et mises à jour, vous pouvez mettre à jour les fichiers source du proxy et créer un nouvel assembly de proxy à l’aide du script GenWCFProxyAssembly.cmd dans le même dossier de téléchargement du Kit de développement. Pour un lien vers le téléchargement du kit SDK, voir la [documentation du développeur Project 2013](project-2013-developer-documentation.md). Pour plus d’informations, voir la section [Ajout d’une référence de service](#pj15_PrerequisitesWCF_AddingServiceReference) . 
  
> [!NOTE]
> Lorsque vous extrayez les fichiers source du proxy de le Source.zip de fichiers, les fichiers dans le `Documentation\IntelliSense\WCF\Source` dossier sont en cours à la date de publication du téléchargement du Kit de développement Project 2013. Pour générer les fichiers de sources de proxy PSI, exécutez le script GenASMXProxyAssembly.cmd sur l’ordinateur Project Server mis à jour. Pour plus d’informations, voir [Ajout d’une référence de service](#pj15_PrerequisitesWCF_AddingServiceReference). 
> 
> Les scripts dans les `Documentation\IntelliSense\ASMX` dossier ne fonctionnent pas pour les applications basées sur WCF. Le script GenASMXProxyAssembly.cmd appelle Wsdl.exe, qui génère des fichiers de code source pour les services ASMX. Les fichiers de proxy ASMX incluent les propriétés et les différentes classes. Par exemple, le service web de ressources basées sur ASMX inclut la classe de **ressource** , tandis que le service de ressources WCF inclut l’interface de la **ressource** , l’interface **ResourceChannel** et la classe **ResourceClient** . 
  
Les espaces de noms arbitraires créés pour les services web ASMX et les services WCF sont les mêmes, afin que le fichier ProjectServerServices.xml pour IntelliSense fonctionne avec l’assembly. Par exemple, l’espace de noms du service de ressource dans l’assembly de proxy basée sur WCF et l’assembly de proxy basées sur ASMX est **SvcResource**. Vous pouvez bien sûr, modifier les noms d’espace de noms — si vous assurer qu’ils correspondent dans l’assembly de proxy et dans le fichier ProjectServerServices.xml IntelliSense.
  
Si un exemple de code utilise un nom différent pour un espace de noms de service PSI, par exemple **ProjectWebSvc**, pour IntelliSense fonctionne vous devez modifier l’exemple pour utiliser **SvcProject** afin que l’espace de noms correspond à l’assembly de proxy. 
  
Avantages de l’utilisation de l’assembly de proxy basée sur WCF sont les suivantes :
  
- Vous pouvez développer la plupart des solutions avec l’assembly de proxy sur un autre ordinateur que l’ordinateur Project Server. Définition d’une référence de service individuelles nécessite développement sur l’ordinateur Project Server.
    
- L’assembly de proxy inclut tous les espaces de noms PSI service, donc vous n’avez pas ajouter plusieurs fichiers proxy.
    
- Si vous ajoutez le fichier ProjectServerServices.xml dans le même répertoire où vous définissez une référence à l’assembly de proxy ProjectServerServices.dll, vous pouvez obtenir des descriptions IntelliSense des membres et classes PSI. Pour plus d’informations, consultez le fichier [ReadMe_IntelliSense] dans le `Documentation\IntelliSense` dossier du téléchargement du Kit de développement Project 2013. 
    
**La figure 2. Utilisation d’IntelliSense pour une méthode dans le service de ressources**

![À l’aide d’Intellisense pour la méthode ReadResource] (media/pj15_PrerequisitesWCF_Intellisense.gif "À l’aide d’Intellisense pour la méthode ReadResource")
  
Inconvénients liés à l’aide de l’assembly de proxy sont la solution est plus importante que vous devez distribuer et installer l’assembly de proxy avec la solution. Vous devez également utiliser les mêmes espaces de noms qui se trouvent dans l’assembly de proxy et les fichiers IntelliSense, sauf si vous modifiez le script pour créer un assembly de proxy et de modifier le fichier ProjectServerServices.xml IntelliSense pour utiliser des espaces de noms différents.
  
### <a name="adding-a-psi-proxy-file"></a>Ajout d’un fichier de proxy PSI
<a name="pj15_PrerequisitesWCF_AddingProxyFile"> </a>

Le téléchargement du Kit de développement Project 2013 inclut les fichiers source sont générés par la commande SvcUtil.exe pour l’assembly de proxy. Les fichiers sources se trouvent dans le fichier Source.zip dans le `Documentation\IntelliSense\WCF` sous-répertoire. Au lieu d’une référence à l’assembly de proxy, vous pouvez ajouter une ou plusieurs des fichiers sources pour une solution Visual Studio. Par exemple, pour utiliser le service de projet et le service de ressources, ajoutez le wcf. Project.cs et wcf. Fichiers Resource.cs à la solution. 
  
Dans WCF, la classe principale dans chaque service PSI est définie par une interface et implémentée dans une classe de client pour l’accès aux membres. Par exemple, l’interface **SvcProject.Resource** est implémenté dans la classe **SvcProject.ResourceClient** . Pour définir un objet **ResourceClient** comme une variable de classe nommée **resourceClient**, par exemple, utilisez le code suivant. Dans l’exemple, la méthode **SetClientEndpoints** crée un objet **resourceClient** qui utilise le point de terminaison **basicHttp_Project** , qui est définie dans le fichier app.config. Pour plus d’informations sur le fichier app.config, consultez la section [Ajout d’un fichier de configuration de service](#pj15_PrerequisitesWCF_AddConfig) . 
  
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
> Si vous utilisez un assembly de proxy PSI ou ajoutez un fichier de proxy pour une référence de service Project nommé **SvcResource**, vous utiliseriez le même code pour créer et supprimer un objet **resourceClient** . 
  
### <a name="adding-a-service-reference"></a>Ajout d’une référence de service
<a name="pj15_PrerequisitesWCF_AddingServiceReference"> </a>

Si vous ne pas utiliser l’assembly de proxy basée sur WCF ou ajouter un fichier de proxy pour un service PSI, vous pouvez définir une ou plusieurs références de service individuelles directement dans Visual Studio. Vous pouvez également utiliser l’étape 1 de la procédure suivante pour créer les fichiers proxy mis à jour, pour préparer le `Documentation\IntelliSense\WCF\GenWCFProxyAssembly.cmd` de script qui est inclus dans le téléchargement du Kit de développement Project 2013. 
  
> [!NOTE]
> Pour définir une référence de service, vous devez utiliser Visual Studio sur l’ordinateur Project Server. Nous vous recommandons d’utiliser l’assembly de proxy ProjectServerServices.dll ou ajouter des fichiers de code source proxy, au lieu d’ajouter directement des références de service dans Visual Studio. 
  
Les étapes suivantes indiquent comment définir une référence de service à l’aide de Visual Studio 2012 sur un ordinateur exécutant une installation de test de Project Server :
  
1. Pour obtenir l’accès aux services WCF principal, exécutez Visual Studio sur l’ordinateur Project Server.
    
2. Dans **L’Explorateur de solutions**, cliquez sur le dossier **références** , puis cliquez sur **Ajouter une référence de Service**. 
    
3. Dans la boîte de dialogue **Ajouter une référence de Service** , dans la zone de texte **adresse** , tapez http://localhost:32843/ _GUID_/psi/ _ServiceName_.svc et appuyez sur **entrée**. Remplacez le _GUID_ par le nom du répertoire virtuel de l’application de service Project Server, tels que 534c37eb00d74ccfadcecf9827e95239. Remplacez _ServiceName_ par le nom du service, telles que des ressources (voir Figure 3). 
    
   Vous pouvez obtenir le nom du répertoire virtuel de Service Project Server dans une des manières suivantes :
    
   - Dans votre navigateur, ouvrez l’application Administration centrale de SharePoint 2013. Sélectionnez **Gérer les applications de service**, puis l’application de Service Project Server PSI que vous souhaitez. Par exemple, choisissez **ProjectServerService**. L’URL de la page Gérer les Sites Project Web App contient le nom du répertoire virtuel. Par exemple, dans `http://ServerName:8080/_admin/pwa/managepwa.aspx?appid=534c37eb-00d7-4ccf-adce-cf9827e95239`, est le nom du répertoire virtuel `534c37eb00d74ccfadcecf9827e95239` (le nom du répertoire ne contient aucun tirets). 
    
   - Ouvrez la boîte de dialogue **Gestionnaire des Services Internet (IIS)** sur l’ordinateur Project Server. Développez le nœud **Services Web SharePoint** dans le volet **connexions** , puis les répertoires virtuels service au-dessous, jusqu'à ce que vous trouviez le répertoire qui contient un dossier PSI. Sélectionnez le répertoire, cliquez sur **Paramètres avancés** dans le volet **Actions** , puis copiez le nom du répertoire dans le champ **Chemin d’accès virtuel** . 
    
      > [!NOTE]
      > Il peut y avoir plusieurs répertoires virtuels de Service Project Server. Assurez-vous de choisir le répertoire virtuel qui contient l’instance Project Web App que vous souhaitez. 
  
   - Utilisez l’applet de commande **get-SPServiceApplication** dans Windows PowerShell qui est installé avec SharePoint 2013. Dans le menu **Démarrer** de la barre des tâches, sélectionnez **Tous les programmes**, cliquez sur **Produits Microsoft SharePoint 2013**, puis **SharePoint 2013 Management Shell**. Voici la commande et les résultats dans la fenêtre de **SharePoint 2013get-Management Shell** pour les applications de service défini (vos GUID sera différente). Copiez le GUID de l’application de service Project Server. 
    
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

      Si vous connaissez le nom complet de l’application de Service Project Server, vous pouvez l’utiliser pour obtenir la valeur du GUID, par exemple :
    
        ```powershell
        PS > $projectService = "ProjectServerService"
        PS > (get-SPServiceApplication -Name $projectService).Id
        Guid
        ----
        534c37eb-00d7-4ccf-adce-cf9827e95239
       ```

      > [!NOTE]
      > Supprimer les tirets dans le GUID pour obtenir le nom du répertoire virtuel. 
  
   URL comme `http://localhost:32843/534c37eb00d74ccfadcecf9827e95239/PSI/Resource.svc` sont standard pour les services de Project Server. 
    
4. Une fois la référence de service est résolu, tapez le nom de référence dans la zone de texte **Namespace** . Exemples de code dans la documentation du développeur Project 2013 utilisent le nom de l’espace de noms arbitraire **Svc _ServiceName_**. Par exemple, le service de ressources dans les exemples de code nommé **SvcResource**.
    
    **La figure 3. Ajout de la référence de service de ressources WCF**

    ![Ajout de la référence de service de ressources WCF] (media/pj15_PrerequisitesWCF_AddSvcReference.gif "Ajout de la référence de service de ressources WCF")
  
5. Remplacez le fichier web.config temporaire dans le répertoire du Service de projet d’origine (renommée web.config), puis réexécutez `iisreset`.
    
## <a name="setting-other-references"></a>Autres références
<a name="pj15_PrerequisitesWCF_OtherReferences"> </a>

Project Server applications utilisent souvent les autres services, tels que des services web de SharePoint 2013. Si d’autres services ou des références sont nécessaires, elles sont indiquées dans l’exemple de code.
  
Références locales pour l’exemple de code sont répertoriés dans les instructions **using** dans la partie supérieure de l’échantillon. 
  
1. Dans **L’Explorateur de solutions**, cliquez sur le dossier **références** , puis cliquez sur **Ajouter une référence**.
    
2. Cliquez sur **Parcourir**, puis naviguez jusqu'à l’emplacement où vous avez stocké les DLL Project Server que vous avez copié précédemment. Choisissez les DLL que vous souhaitez, puis cliquez sur **OK**.
    
> [!NOTE]
> Assurez-vous que les versions de l’assembly sur votre ordinateur de développement correspond exactement à ceux présents sur l’ordinateur de Project Server cible. 
  
## <a name="adding-a-service-configuration-file"></a>Ajout d’un fichier de configuration de service
<a name="pj15_PrerequisitesWCF_AddConfig"> </a>

Si une application configure par programme les services WCF, il n’utilise pas un fichier de configuration de service. Dans le cas contraire, une application Windows ou une application console utilise l’élément **system.serviceModel** dans un fichier app.config ; une application web inclut **system.serviceModel** dans le fichier web.config. Pour plus d’informations sur l’utilisation d’un fichier app.config ou de configuration par programme des services WCF, consultez la rubrique [procédure pas à pas : applications PSI développement à l’aide de WCF](http://msdn.microsoft.com/library/65707234-c3da-44e4-8364-32a6be28f645%28Office.15%29.aspx).
  
Lorsqu’il génère un fichier source proxy de service, la commande SvcUtil.exe crée également un fichier output.config qui sert de base à l’élément de **system.serviceModel** par défaut dans un fichier app.config ou le fichier web.config. Le téléchargement du Kit de développement Project 2013 inclut un exemple de fichier output.config dans `Documentation\IntelliSense\WCF\Source.zip`. Par exemple, le fichier output.config par défaut SvcUtil.exe crée pour le service de ressources comprend deux liaisons, nommés **BasicHttpBinding_Resource** et **BasicHttpBinding_Resource1**. L’élément **client** inclut deux points de terminaison par défaut. Un point de terminaison est pour sécuriser l’accès à l’adresse HTTP sur le port 32843 et l’autre pour l’accès normal sur le port 32843, comme suit : 
  
```XML
<client>
    <endpoint address="http://ServerName.domain:32843/GUID/PSI/Resource.svc/secure"
        binding="basicHttpBinding" bindingConfiguration="BasicHttpBinding_Resource"
        contract="SvcResource.Resource" name="BasicHttpBinding_Resource" />
address="http://ServerName.domain:32843/GUID/PSI/Resource.svc"
        binding="basicHttpBinding" bindingConfiguration="BasicHttpBinding_Resource1"
        contract="SvcResource.Resource" name="BasicHttpBinding_Resource1" />
</client>
```

Configuration du service PSI n’utilise pas les liaisons par défaut et les points de terminaison. Project Server requiert que les applications accès services PSI via la ProjectServer.svc frontal, qui joue le rôle de routeur pour les appels vers les services de serveur principal. Pour créer le fichier app.config, procédez comme suit :
  
1. Si vous définissez une référence à l’assembly de proxy ProjectServerServices.dll, ou ajoutez le fichier source de proxy pour un service, l’application ne contient pas un fichier app.config. Ajouter un nouvel élément au projet Visual Studio. Dans la boîte de dialogue **Ajouter un nouvel élément** , choisissez le modèle de **Fichier de Configuration de l’Application** , nommez-le app.config, puis choisissez **Ajouter**.
    
2. Supprimez tout le texte dans le fichier app.config, puis copiez le code suivant dans le fichier. Vous pouvez utiliser la même liaison, par exemple `basicHttpConf`, pour chaque point de terminaison de service. Si vous souhaitez utiliser plus d’une liaison, par exemple, pour lier les protocoles HTTP et HTTPS, vous devez créer une liaison pour chaque protocole.
    
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
                                <transport clientCredentialType="Ntlm" realm="http://SecurityDomain" />
                            </security>
                        </binding>
                    </basicHttpBinding>
                </bindings>
                <client>
                    <endpoint address="http://ServerName/ProjectServerName/_vti_bin/PSI/ProjectServer.svc"
                        behaviorConfiguration="basicHttpBehavior" binding="basicHttpBinding"
                        bindingConfiguration="basicHttpConf" 
                        contract="SvcServiceName.ServiceName"
                        name="basicHttp_ServiceName" />
                </client>
            </system.serviceModel>
        </configuration>
    ```

3. Remplacez `ServerName/ProjectServerName` dans l’adresse du point de terminaison client avec le nom de votre serveur et l’instance Project Web App. 
    
4. Remplacez `ServiceName` avec le nom du service PSI, telles que des ressources. Veillez à remplacer les trois instances du nom du service, par exemple :
    
    ```XML
        <endpoint address="http://myserver/pwa/_vti_bin/PSI/ProjectServer.svc"
            behaviorConfiguration="basicHttpBehavior" binding="basicHttpBinding"
            bindingConfiguration="basicHttpConf" 
            contract="SvcResource.Resource"
            name="basicHttp_Resource" />
    ```

5. Pour utiliser plus de service PSI un, créez un élément de **point de terminaison** pour chaque service et pour chaque élément de **liaison** qui utilise des services. Par exemple, les points de terminaison suivantes configurer le client pour utiliser la liaison HTTP de base pour le service de projet et le service QueueSystem. 
    
    > [!NOTE]
    > Si vous exécutez une application et un message d’erreur que le serveur est trop occupé ou que la demande HTTP n’est pas autorisée, assurez-vous que les adresses de point de terminaison sont correctes dans le fichier app.config. 
  
    ```XML
        <client>
        <endpoint address="http://ServerName/pwa/_vti_bin/PSI/ProjectServer.svc"
            behaviorConfiguration="basicHttpBehavior" binding="basicHttpBinding"
            bindingConfiguration="basicHttpConf" 
            contract="SvcProject.Project"
            name="basicHttp_Project" />
        <endpoint address="http://ServerName/pwa/_vti_bin/PSI/ProjectServer.svc"
            behaviorConfiguration="basicHttpBehavior" binding="basicHttpBinding"
            bindingConfiguration="basicHttpConf" 
            contract="SvcQueueSystem.QueueSystem"
            name="basicHttp_QueueSystem" />
        </client>
    ```

Vous pouvez modifier un fichier app.config à l’aide de l' **Éditeur de Configuration du Service WCF** dans Visual Studio (dans le menu **Outils** ). La figure 4 montre comment définir l’élément **contrat** dans la boîte de dialogue **Éditeur de Configuration du Service Microsoft** . Si la solution à l’aide de l’assembly de proxy PSI, ouvrez ProjectServerServices.dll dans le `bin\debug` répertoire de la solution Visual Studio. La boîte de dialogue **Explorateur de types de contrat** affiche tous les contrats de service WCF (voir la Figure 5). 
  
**La figure 4. À l’aide de l’éditeur de Configuration du Service WCF**

![À l’aide de l’éditeur de Configuration du Service WCF] (media/pj15_PrerequisitesWCF_ServiceConfigurationEditor.gif "À l’aide de l’éditeur de Configuration du Service WCF")
  
Si la solution utilise un fichier de proxy de service, tels que wcfResource.cs, compilez l’application et ouvrez le fichier exécutable dans le `bin\debug` directory. Pour plus d’informations sur la modification du fichier app.config, consultez la rubrique [procédure pas à pas : applications PSI développement à l’aide de WCF](http://msdn.microsoft.com/library/65707234-c3da-44e4-8364-32a6be28f645%28Office.15%29.aspx).
  
**La figure 5. Dans l’éditeur de Configuration de Service WCF à l’aide de l’Explorateur de types de contrat**

![À l’aide de l’Explorateur de types de contrat] (media/pj15_PrerequisitesWCF_ContractTypeBrowser.gif "À l’aide de l’Explorateur de types de contrat")
  
## <a name="using-multiple-authentication"></a>À l’aide de l’authentification multiples
<a name="pj15_PrerequisitesWCF_ClaimsMultiAuth"> </a>

L’authentification des utilisateurs de Project Server sur site, par l’authentification Windows ou l’authentification par formulaires, s’effectue par le biais de réclamations dans SharePoint. Authentification plusieurs signifie que l’application web sur lequel est mis en service Project Web App prend en charge l’authentification Windows et l’authentification basée sur les formulaires. Si tel est le cas, tout appel à un service WCF qui utilise l’authentification Windows échoue avec l’erreur suivante, car le processus ne peut pas déterminer le type d’authentification utilisateur :
  
`The server was unable to process the request due to an internal error. For more information about the error, either turn on Include ExceptionDetailInFaults (either from ServiceBehaviorAttribute or from the <serviceDebug> configuration behavior) on the server in order to send the exception information back to the client, or turn on tracing as per the Microsoft .NET Framework 3.0 SDK documentation and inspect the server trace logs.`

Pour résoudre le problème pour WCF, tous les appels aux méthodes PSI doivent être dans un **OperationContextScope** qui est définie pour chaque service PSI. Ne pas imbriquer des étendues pour plusieurs services ; par exemple, lorsque vous utilisez les appels vers les services de ressources et des projets, chaque jeu d’appels doit être dans sa propre portée. 
  
Dans l’exemple suivant, la méthode **DisableFormsAuth** peut être appelée à partir de chaque section **OperationContextScope** dans une application. La méthode supprime toute valeur en-tête auparavant désactivé l’authentification par formulaires, afin que l’authentification par formulaires peut s’exécuter si le paramètre _isWindowsAuth_ est **false**. Si _isWindowsAuth_ a la **valeur true**, la méthode **DisableFormsAuth** désactive l’authentification par formulaires. 
  
Dans la méthode **WcfSample** , l’objet **projectClient** est une instance de la classe PSI **SvcProject.ProjectClient** . 
  
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
> Appels PSI dans un **OperationContextScope** est requis uniquement pour les applications qui s’exécutent dans un environnement d’authentification. Si Project Server utilise uniquement l’authentification Windows, il n’est pas nécessaire de définir une étendue et ajouter un en-tête de requête web qui désactive l’authentification par formulaires. 
> 
> Le correctif pour une application basées sur ASMX est différent. Pour plus d’informations, consultez la section *authentifications multiples à l’aide* de [conditions préalables pour les exemples de code basées sur ASMX dans Project](prerequisites-for-asmx-based-code-samples-in-project.md). 
  
## <a name="changing-values-of-generic-constants"></a>Modification des valeurs des constantes génériques
<a name="pj15_PrerequisitesWCF_ChangeValues"> </a>

La plupart des exemples ont une ou plusieurs variables que vous devez mettre à jour pour l’exemple de fonctionner correctement dans votre environnement. Dans l’exemple suivant, si vous avez installé SSL, utilisez le protocole HTTPS au lieu du protocole HTTP. Remplacez _ServerName_ par le nom du serveur que vous utilisez. Remplacez _ProjectServerName_ par le nom du répertoire virtuel de votre site project server, tels que PWA. 
  
```cs
const string PROJECT_SERVER_URI = "http://ServerName/ProjectServerName/";
```

Toutes les variables que vous devez modifier sont indiquées dans la partie supérieure de l’exemple de code.
  
## <a name="verifying-the-results"></a>Vérification des résultats
<a name="pj15_PrerequisitesWCF_Verify"> </a>

Obtention et l’interprétation des résultats à partir d’un exemple de code ne sont pas toujours simple. Par exemple, si vous créez un projet, vous devez publier le projet avant d’apparaître dans la page Centre de projets dans Project Web App.
  
Vous pouvez vérifier les résultats des exemples de code de plusieurs façons, par exemple :
  
- Utilisez le client Project Professional 2013 pour ouvrir le projet à partir de l’ordinateur Project Server et afficher les éléments que vous souhaitez.
    
- Afficher les projets publiés sur la page Centre de projets de Project Web App ( `http://ServerName/ProjectServerName/projects.aspx`).
    
- Afficher le journal de file d’attente dans Project Web App. Ouvrez la page Paramètres du serveur (dans le coin supérieur droit, choisissez l’icône **paramètres** ), puis cliquez sur **Mes travaux en file d’attente** sous la section **Paramètres personnels** ( `http://ServerName/ProjectServerName/MyJobs.aspx`). Dans la liste déroulante **affichage** , vous pouvez trier par l’état du travail. L’état par défaut est **en cours et l’échec des travaux de la semaine**. 
    
- Utilisez la page Paramètres du serveur dans Project Web App ( `http://ServerName/ProjectServerName/_layouts/15/pwa/admin/admin.aspx`) pour gérer tous les travaux en file d’attente et de supprimer ou de forcer l’archivage des objets d’entreprise. Vous devez disposer des autorisations d’administration pour accéder à ces liens dans la page Paramètres du serveur.
    
- **Microsoft SQL Server Management Studio** permet d’exécuter une requête sur une table de base de données Project Server. Par exemple, utilisez la requête suivante pour sélectionner les 200 premières lignes de la table MSP_WORKFLOW_STAGE_PDPS pour afficher des informations sur les pages de détails de projet (PDP) dans les étapes de flux de travail. 
    
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

Après avoir testé des exemples de code, des objets d’entreprise et qui doivent être supprimés ou réinitialiser les paramètres. Vous pouvez utiliser la page Paramètres du serveur dans Project Web App pour gérer les données d’entreprise ( `http://ServerName/ProjectServerName/_layouts/15/pwa/admin/admin.aspx`). Liens dans la page Paramètres du serveur permettent de supprimer les anciens éléments, forcer l’archivage des projets, gérer la file d’attente pour tous les utilisateurs et effectuer d’autres tâches d’administration.
  
Voici certains des liens dans la page Paramètres du serveur à utiliser pour les activités de nettoyage par défaut après l’exécution des exemples de code :
  
- **Tables de choix et champs personnalisés d’entreprise**
    
- **Gérer les travaux de file d’attente**
    
- **Supprimer des objets d’entreprise**
    
- **Forcer l’archivage des objets d’entreprise**
    
- **Types de projets d’entreprise**
    
- **Phases du flux de travail**
    
- **Étapes du flux de travail**
    
- **Pages de détails de projet**
    
- **Périodes de rapports**
    
- **Valeurs par défaut et les paramètres de la feuille de temps**
    
- **Classifications de lignes**
    
Paramètres supplémentaires sont gérés par SharePoint Server 2013 pour chaque instance de Project Web App, plutôt que par une page spécifique de paramètres de Project Web App. Dans l’application Administration centrale de SharePoint, sélectionnez **Paramètres généraux de l’Application**, cliquez sur **Gérer les** sous **Paramètres de Project Server**, puis l’instance Project Web App dans la liste déroulante dans la page Paramètres du serveur . Par exemple, choisissez de **Gestionnaires d’événements côté serveur** pour ajouter ou supprimer des gestionnaires d’événements pour l’instance Project Web App sélectionnée. 
  
## <a name="see-also"></a>Voir aussi

- [Conditions préalables pour les exemples de code basées sur ASMX dans Project](prerequisites-for-asmx-based-code-samples-in-project.md)   
- [Procédure pas à pas : Développement d’applications PSI à l’aide de WCF](http://msdn.microsoft.com/library/65707234-c3da-44e4-8364-32a6be28f645%28Office.15%29.aspx)   
- [Utiliser l’emprunt d’identité avec WCF](http://msdn.microsoft.com/library/e3597901-2f02-44a2-8076-d32aae540b38%28Office.15%29.aspx)  
- [Présentation des références de projet PSI](project-psi-reference-overview.md) 
- [Centre pour développeurs SharePoint](http://msdn.microsoft.com/en-us/sharepoint/default.aspx)
    

