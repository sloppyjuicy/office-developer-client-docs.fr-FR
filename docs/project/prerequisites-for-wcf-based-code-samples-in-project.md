---
title: Conditions préalables pour les exemples de code basés sur WCF
manager: soliver
ms.date: 09/17/2015
ms.audience: Developer
localization_priority: Normal
ms.assetid: 60d2afc8-10b6-465d-8ce8-c073da6e5054
description: Découvrez des informations pour vous aider à créer des projets dans Visual Studio à l'aide des exemples de code basés sur WCF qui sont inclus dans les rubriques de référence de l'interface PSI (Project Server Interface).
ms.openlocfilehash: 2222e1b3651044c41f45e57481f80093aac67bdb
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32357155"
---
# <a name="prerequisites-for-wcf-based-code-samples-in-project"></a>Conditions préalables pour les exemples de code basés sur WCF

Découvrez des informations pour vous aider à créer des projets dans Visual Studio à l'aide des exemples de code basés sur WCF qui sont inclus dans les rubriques de référence de l'interface PSI (Project Server Interface).
   
De nombreux exemples de code basés sur WCF inclus dans la [bibliothèque de classes de Project Server 2013 et la référence de service Web](https://msdn.microsoft.com/library/ef1830e0-3c9a-4f98-aa0a-5556c298e7d1%28Office.15%29.aspx) ont été créés à l'origine pour la documentation du développeur Project 2010 et utilisent un format standard pour les services Web WCF. Les exemples fonctionnent toujours dans Project Server 2013 et sont conçus pour être copiés dans une application console et exécutés en tant qu'unité complète. Les exceptions sont indiquées dans l'exemple. 
  
Les exemples de code dans la documentation du développeur Project 2013 qui ne sont pas modifiés à partir des exemples développés pour Office Project Server 2007 utilisent les services Web ASMX. Les exemples basés sur ASMX peuvent également être adaptés pour utiliser les services WCF. Cet article explique comment utiliser les exemples avec les services WCF. Pour plus d'informations sur l'utilisation des exemples avec les services Web ASMX, reportez-vous à la rubrique [Prerequisites for asmx-based Code Samples in Project](prerequisites-for-asmx-based-code-samples-in-project.md).
  
> [!NOTE]
> Si le modèle objet côté client (CSOM) inclut les méthodes dont votre application a besoin, les nouvelles applications doivent être développées avec le CSOM. Le CSOM permet aux applications de fonctionner avec Project Online ou une installation locale de Project Server 2013. Dans le cas contraire, si votre application utilise la PSI, elle doit utiliser l'interface WCF, qui est la technologie recommandée pour les communications réseau. Les applications qui utilisent l'interface ASMX ou l'interface WCF peuvent fonctionner uniquement pour les installations locales de Project Server 2013. 
>
> Pour plus d'informations sur les CSOM, consultez la rubrique [Project Server 2013 architecture](project-server-2013-architecture.md) and [Client-Side Object Model (CSOM) for Project 2013](client-side-object-model-csom-for-project-2013.md). 
  
Avant d'exécuter les exemples de code, vous devez configurer l'environnement de développement, configurer l'application, ajouter un fichier de configuration de service (ou configurer les services WCF par programme) et modifier les valeurs des constantes génériques en fonction de votre environnement.
  
## <a name="setting-up-the-development-environment"></a>Configuration de l'environnement de développement
<a name="pj15_PrerequisitesWCF_Setup"> </a>

1. **ConFigurez un système Project Server de test.**
    
    Utilisez un système Project Server de test chaque fois que vous effectuez des tests ou des développements. Même si votre code fonctionne parfaitement, les dépendances entre projets, la création de rapports ou d'autres facteurs environnementaux peuvent avoir des conséquences inattendues. 
    
    > [!NOTE]
    > Assurez-vous que vous êtes un utilisateur valide sur le serveur et vérifiez que vous disposez des autorisations suffisantes pour les appels PSI que votre application utilise. La rubrique relative à la documentation du développeur pour chaque méthode PSI comprend une table d'autorisations Project Server. Par exemple, la méthode [Project. QueueCreateProject](https://msdn.microsoft.com/library/WebSvcProject.Project.QueueCreateProject.aspx) nécessite l'autorisation globale **NewProject** et l'autorisation **SaveProjectTemplate** . 
  
    Dans certains cas, vous devrez peut-être effectuer un débogage à distance sur le serveur. Vous devrez peut-être également configurer un gestionnaire d'événements en installant un assembly de gestionnaire d'événements sur chaque ordinateur Project Server de la batterie de serveurs SharePoint, puis en configurant le gestionnaire d'événements pour l'instance de Project Web App à l'aide de la page Paramètres de Project Server dans le grand Paramètres d'application de l'administration centrale de SharePoint.
    
2. **ConFigurez un ordinateur de développement.**
    
    En règle générale, vous accédez à l'interface PSI via un réseau. Les exemples de code sont conçus pour être exécutés sur un client distinct du serveur, sauf indication contraire.
    
    1. **Installez la version appropriée de Visual Studio.** Sauf indication contraire, les exemples de code sont écrits en Visual C#. Elles peuvent être utilisées avec Visual Studio 2010 ou Visual Studio 2012. Assurez-vous que le Service Pack le plus récent est installé. 
    
    2. **Copiez les dll Project Server sur l'ordinateur de développement.** Copiez les assemblys suivants `[Program Files]\Microsoft Office Servers\15.0\Bin` de sur l'ordinateur Project Server vers l'ordinateur de développement: 
    
       - Microsoft.Office.Project.Server.Events.Receivers.dll
    
       - Microsoft.Office.Project.Server.Library.dll
    
    3. Pour plus d'informations sur la compilation et l'utilisation de l'assembly de proxy ProjectServerServices. dll pour les services WCF dans le PSI, voir [utilisation d'un assembly de proxy PSI et descriptions IntelliSense](#pj15_PrerequisitesWCF_BuildingProxy).
    
3. **Installez les fichiers IntelliSense.**
    
    Pour utiliser les descriptions IntelliSense pour les classes et les membres des assemblys Project Server, copiez les fichiers XML IntelliSense mis à jour à partir du téléchargement du kit de développement logiciel (SDK) Project 2013 dans le même répertoire où se trouvent les assemblys Project Server. Par exemple, copiez le fichier Microsoft. Office. Project. Server. Library. xml dans le répertoire dans lequel votre application définira une référence à l'assembly Microsoft. Office. Project. Server. Library. dll.
    
    Pour les services PSI, les descriptions IntelliSense vous obligent à créer un assembly de proxy PSI à l'aide du `Documentation\IntelliSense\WCF` script CompileWCFProxyAssembly. cmd dans le sous-répertoire du téléchargement du kit de développement logiciel (SDK) de Project 2013. Le script crée l'assembly de proxy ProjectServerServices. dll basé sur WCF. Pour plus d'informations, consultez le fichier [ReadMe_IntelliSense]. mht dans le téléchargement du kit de développement logiciel (SDK). 
    
## <a name="creating-the-application-and-adding-a-service-reference"></a>Création de l'application et ajout d'une référence de service
<a name="pj15_PrerequisitesWCF_Configure"> </a>

1. **Créez une application console.**
    
    Lorsque vous créez une application console, dans la liste déroulante de la boîte de dialogue **nouveau projet** , sélectionnez **.NET Framework 4**. Vous pouvez copier l'exemple de code PSI dans la nouvelle application.
    
2. **Ajoutez les références requises pour WCF.**
    
    Dans l'Explorateur de solutions, ajoutez une référence à **System. ServiceModel** (voir figure 1). Une application Web utilise **System. ServiceModel. Web**.
    
    Ajoutez également une référence à **System. Runtime. Serialization**.
    
    **Figure 1. Ajout de références dans Visual Studio pour une application basée sur WCF**

    ![Ajout de références pour WCF] (media/pj15_PrerequisitesWCF_AddReference.gif "Ajout de références pour WCF")
  
3. **Copiez le code**.
    
    Copiez l'exemple de code complet dans le fichier Program.cs de l'application console.
    
4. **Définissez l'espace de noms pour l'exemple d'application.**
    
    Vous pouvez modifier l'espace de noms mentionné en haut de l'exemple pour l'espace de noms de l'application par défaut ou modifier l'espace de noms de l'application par défaut pour qu'il corresponde à l'exemple. Vous pouvez modifier l'espace de noms de l'application par défaut en modifiant les propriétés de l'application. 
    
    Par exemple, l'exemple de code pour [ReadResource](https://msdn.microsoft.com/library/WebSvcResource.Resource.ReadResource.aspx) a l'espace de noms **Microsoft. Sdk. Project. Samples. CreateResourceTest**. Si le nom du projet Visual Studio est **ResourceTest**, copiez l'espace de noms à partir du fichier Program.cs, puis ouvrez le volet **Propriétés** du projet (dans le menu **projet** , choisissez **Propriétés ResourceTest**). Dans l'onglet **application** , copiez l'espace de noms dans la zone de texte **espace de noms par défaut** . 
    
5. **Définissez les références de service.**
    
    De nombreux exemples nécessitent une référence à un ou plusieurs des services PSI. Celles-ci sont répertoriées dans l'exemple lui-même ou dans les commentaires qui précèdent l'exemple. Pour obtenir l'espace de noms approprié des références de service, assurez-vous d'abord de définir l'espace de noms de l'application par défaut.
    
    Il existe trois façons d'ajouter une référence de service WCF:
    
    - Créez un assembly de proxy PSI nommé ProjectServerServices. dll, puis définissez une référence à l'assembly. Voir [utilisation d'un assembly de proxy PSI et descriptions IntelliSense](#pj15_PrerequisitesWCF_BuildingProxy).
    
    - Ajoutez un fichier proxy à partir de la sortie Svcutil. exe vers la solution Visual Studio. Consultez [la rubrique Ajout d'un fichier proxy PSI](#pj15_PrerequisitesWCF_AddingProxyFile).
    
    - Ajoutez une référence de service à l'aide de Visual Studio. Consultez [la rubrique Ajout d'une référence de service](#pj15_PrerequisitesWCF_AddingServiceReference).
    
### <a name="using-a-psi-proxy-assembly-and-intellisense-descriptions"></a>Utilisation d'un assembly de proxy PSI et descriptions IntelliSense
<a name="pj15_PrerequisitesWCF_BuildingProxy"> </a>

Vous pouvez utiliser un assembly de proxy pour tous les services WCF publics dans le PSI. ComPilez l'assembly de proxy ProjectServerServices. `Documentation\IntelliSense\WCF\CompileWCFProxyAssembly.cmd` dll à l'aide du script du kit de développement logiciel (SDK) de Project 2013, puis copiez l'assembly de proxy sur votre ordinateur de développement. Copiez le fichier ProjectServerServices. xml pour IntelliSense au même emplacement. Dans Visual Studio, définissez une référence à l'assembly de proxy ProjectServerServices. dll. 
  
Pour les service packs et les mises à jour de Project Server, vous pouvez mettre à jour les fichiers sources du proxy et créer un assembly de proxy à l'aide du script GenWCFProxyAssembly. cmd dans le même dossier de téléchargement du kit SDK. Pour obtenir un lien vers le téléchargement du kit de développement logiciel (SDK), consultez la [documentation du développeur Project 2013](project-2013-developer-documentation.md). Pour plus d'informations, consultez la section [Ajout d'une référence de service](#pj15_PrerequisitesWCF_AddingServiceReference) . 
  
> [!NOTE]
> Lorsque vous extrayez les fichiers sources proxy à partir du fichier. zip source, les `Documentation\IntelliSense\WCF\Source` fichiers du dossier sont actualisés à la date de publication du téléchargement du kit de développement logiciel (SDK) Project 2013. Pour générer des fichiers sources de proxy PSI mis à jour, exécutez le script GenASMXProxyAssembly. cmd sur l'ordinateur Project Server. Pour plus d'informations, consultez [la rubrique Ajout d'une référence de service](#pj15_PrerequisitesWCF_AddingServiceReference). 
> 
> Les scripts du `Documentation\IntelliSense\ASMX` dossier ne fonctionnent pas pour les applications basées sur WCF. Le script GenASMXProxyAssembly. cmd appelle wsdl. exe, qui génère des fichiers de code source pour les services ASMX. Les fichiers proxy ASMX incluent différentes classes et propriétés. Par exemple, le service Web de ressource ASMX inclut la classe de **ressource** , tandis que le service de ressources basées sur WCF inclut l'interface de **ressource** , l'interface **ResourceChannel** et la classe **ResourceClient** . 
  
Les espaces de noms arbitraires créés pour les services Web ASMX et les services WCF sont les mêmes, de sorte que le fichier ProjectServerServices. xml pour IntelliSense fonctionne avec l'un ou l'autre assembly. Par exemple, l'espace de noms du service de ressources dans l'assembly de proxy basé sur WCF et dans l'assembly de proxy ASMX est **SvcResource**. Vous pouvez bien sûr modifier les noms d'espace de noms — si vous vous assurez qu'ils correspondent dans l'assembly de proxy et dans le fichier ProjectServerServices. XML IntelliSense.
  
Si un exemple de code utilise un nom différent pour un espace de noms de service PSI, par exemple **ProjectWebSvc**, pour qu'IntelliSense fonctionne, vous devez modifier l'exemple afin qu'il utilise **SvcProject** afin que l'espace de noms corresponde à l'assembly de proxy. 
  
Les avantages de l'utilisation de l'assembly de proxy basé sur WCF sont les suivants:
  
- Vous pouvez développer la plupart des solutions avec l'assembly de proxy sur un autre ordinateur que l'ordinateur Project Server. La définition d'une référence de service spécifique nécessite un développement sur l'ordinateur Project Server.
    
- L'assembly de proxy inclut tous les espaces de noms de service PSI, de sorte que vous n'avez pas besoin d'ajouter plusieurs fichiers proxy.
    
- Si vous ajoutez le fichier ProjectServerServices. xml dans le même répertoire où vous avez défini une référence à l'assembly de proxy ProjectServerServices. dll, vous pouvez obtenir des descriptions IntelliSense pour les classes et les membres PSI. Pour plus d'informations, reportez-vous au fichier `Documentation\IntelliSense` [ReadMe_IntelliSense] dans le dossier du téléchargement du kit de développement logiciel (SDK) Project 2013. 
    
**Figure 2. Utilisation d'IntelliSense pour une méthode dans le service de ressources**

![Utilisation d'IntelliSense pour la méthode ReadResource] (media/pj15_PrerequisitesWCF_Intellisense.gif "Utilisation d'IntelliSense pour la méthode ReadResource")
  
Les inconvénients de l'utilisation de l'assembly de proxy sont les suivants: la solution est plus grande et vous devez distribuer et installer l'assembly de proxy avec la solution. Vous devez également utiliser les mêmes espaces de noms que ceux qui se trouvent dans l'assembly de proxy et les fichiers IntelliSense, sauf si vous modifiez le script pour générer un assembly de proxy et modifier le fichier ProjectServerServices. XML IntelliSense de sorte qu'il utilise des espaces de noms différents.
  
### <a name="adding-a-psi-proxy-file"></a>Ajout d'un fichier proxy PSI
<a name="pj15_PrerequisitesWCF_AddingProxyFile"> </a>

Le téléchargement du kit de développement logiciel (SDK) Project 2013 inclut les fichiers sources générés par la commande SvcUtil. exe pour l'assembly de proxy. Les fichiers sources se trouvent dans le fichier. zip source dans `Documentation\IntelliSense\WCF` le sous-répertoire. Au lieu de définir une référence à l'assembly de proxy, vous pouvez ajouter un ou plusieurs fichiers sources à une solution Visual Studio. Par exemple, pour utiliser le service de projet et le service de ressources, ajoutez le service WCF. Project.cs et WCF. Resource.cs fichiers de la solution. 
  
Dans WCF, la classe principale de chaque service PSI est définie par une interface et implémentée dans une classe cliente pour accéder aux membres. Par exemple, l'interface **SvcProject. Resource** est implémentée dans la classe **SvcProject. ResourceClient** . Pour définir un objet **ResourceClient** en tant que variable de classe nommée **ResourceClient**, par exemple, utilisez le code suivant. Dans l'exemple, la méthode **SetClientEndpoints** crée un objet **ResourceClient** qui utilise le point de terminaison **basicHttp_Project** , qui est défini dans le fichier app. config. Pour plus d'informations sur le fichier app. config, voir la section relative à l' [Ajout d'un fichier de configuration de service](#pj15_PrerequisitesWCF_AddConfig) . 
  
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
> Que vous utilisiez un assembly de proxy PSI ou que vous ajoutiez un fichier proxy pour une référence de service Project nommée **SvcResource**, vous devez utiliser le même code pour créer et supprimer un objet **ResourceClient** . 
  
### <a name="adding-a-service-reference"></a>Ajout d’une référence de service
<a name="pj15_PrerequisitesWCF_AddingServiceReference"> </a>

Si vous n'utilisez pas l'assembly de proxy basé sur WCF ou si vous ajoutez un fichier proxy pour un service PSI, vous pouvez définir une ou plusieurs références de service individuelles directement dans Visual Studio. Vous pouvez également utiliser l'étape 1 de la procédure suivante pour créer des fichiers proxy mis à jour, `Documentation\IntelliSense\WCF\GenWCFProxyAssembly.cmd` afin de préparer le script inclus dans le téléchargement du kit de développement logiciel (SDK) de Project 2013. 
  
> [!NOTE]
> Pour définir une référence de service, vous devez utiliser Visual Studio sur l'ordinateur Project Server. Nous vous recommandons d'utiliser l'assembly de proxy ProjectServerServices. dll ou d'ajouter des fichiers sources de proxy, au lieu d'ajouter directement des références de service dans Visual Studio. 
  
Les étapes suivantes montrent comment définir une référence de service à l'aide de Visual Studio 2012 sur un ordinateur exécutant une installation de test de Project Server:
  
1. Pour accéder aux services WCF principaux, exécutez Visual Studio sur l'ordinateur Project Server.
    
2. Dans l' **Explorateur de solutions**, cliquez avec le bouton droit sur le dossier **références** , puis choisissez Ajouter une **référence de service**. 
    
3. Dans la boîte de dialogue **Ajouter une référence de service** , dans la zone de texte **adresse** , tapez https://localhost:32843/ _GUID_/PSI/ _ServiceName_. svc, puis appuyez sur **entrée**. Remplacez _GUID_ par le nom du répertoire virtuel de l'application de service Project Server, par exemple 534c37eb00d74ccfadcecf9827e95239. Remplacez _ServiceName_ par le nom du service, tel que Resource (voir figure 3). 
    
   Vous pouvez obtenir le nom du répertoire virtuel du service Project Server en procédant de l'une des manières suivantes:
    
   - Ouvrez l'application Administration centrale de SharePoint 2013 dans votre navigateur. Choisissez **gérer les applications de service**, puis choisissez l'application de service Project Server psi de votre choix. Par exemple, choisissez **ProjectServerService**. L'URL de la page gérer les sites Project Web App contient le nom du répertoire virtuel. Par exemple, dans `https://ServerName:8080/_admin/pwa/managepwa.aspx?appid=534c37eb-00d7-4ccf-adce-cf9827e95239`, le nom du répertoire virtuel `534c37eb00d74ccfadcecf9827e95239` est (le nom du répertoire ne contient pas de tirets). 
    
   - Ouvrez la boîte de dialogue **Gestionnaire des services IIS (Internet Information Services)** sur l'ordinateur Project Server. Développez le nœud des **services Web SharePoint** dans le volet **connexions** , puis développez les répertoires virtuels de service ci-dessous, jusqu'à ce que vous trouviez le répertoire qui inclut un dossier psi. Sélectionnez le répertoire, choisissez **Paramètres avancés** dans le volet **actions** , puis copiez le nom du répertoire dans le champ **chemin d'accès virtuel** . 
    
      > [!NOTE]
      > Il peut y avoir plusieurs répertoires virtuels de service Project Server. Assurez-vous de choisir le répertoire virtuel qui contient l'instance Project Web App de votre choix. 
  
   - Utilisez la cmdlet **Get-SPServiceApplication** dans Windows PowerShell qui est installé avec SharePoint 2013. Dans le menu **Démarrer** de la barre des tâches, choisissez **tous les programmes**, **produits Microsoft SharePoint 2013**, puis sélectionnez **SharePoint 2013 Management Shell**. Voici la commande et les résultats dans la fenêtre **SharePoint 2013get-Management Shell** pour les applications de service définies (vos GUID seront différents). Copiez le GUID de l'application de service Project Server. 
    
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

      Si vous possédez le nom complet de l'application de service Project Server, vous pouvez l'utiliser pour obtenir la valeur GUID, par exemple:
    
        ```powershell
        PS > $projectService = "ProjectServerService"
        PS > (get-SPServiceApplication -Name $projectService).Id
        Guid
        ----
        534c37eb-00d7-4ccf-adce-cf9827e95239
       ```

      > [!NOTE]
      > Supprimez les tirets dans le GUID pour obtenir le nom du répertoire virtuel. 
  
   Les URL telles `https://localhost:32843/534c37eb00d74ccfadcecf9827e95239/PSI/Resource.svc` que standard pour les services Project Server. 
    
4. Une fois que la référence de service est résolue, tapez le nom de la référence dans la zone de texte **espace de noms** . Les exemples de code dans la documentation du développeur Project 2013 utilisent le nom de l'espace de noms arbitraire ** _ServiceName_**. Par exemple, le service de ressources dans les exemples de code est nommé **SvcResource**.
    
    **Figure 3. Ajout de la référence de service de ressources basées sur WCF**

    ![Ajout de la référence de service de ressources basées sur WCF] (media/pj15_PrerequisitesWCF_AddSvcReference.gif "Ajout de la référence de service de ressources basées sur WCF")
  
5. Remplacez le fichier Web. config temporaire dans le répertoire du service Project par l'original (renommé en Web. config), puis réexécutez `iisreset`.
    
## <a name="setting-other-references"></a>Définition d'autres références
<a name="pj15_PrerequisitesWCF_OtherReferences"> </a>

Les applications Project Server utilisent souvent d'autres services, tels que les services Web SharePoint 2013. Si d'autres services ou références sont requis, ils sont indiqués dans l'exemple de code.
  
Les références locales de l'exemple de code sont répertoriées dans instructions **using** en haut de l'exemple. 
  
1. Dans l' **Explorateur de solutions**, cliquez avec le bouton droit sur le dossier **références** , puis choisissez Ajouter une **référence**.
    
2. Choisissez **Parcourir**, puis accédez à l'emplacement où vous avez stocké les dll Project Server que vous avez copiées précédemment. Choisissez les dll de votre choix, puis cliquez sur **OK**.
    
> [!NOTE]
> Assurez-vous que les versions d'assembly de votre ordinateur de développement correspondent exactement à celles de l'ordinateur Project Server cible. 
  
## <a name="adding-a-service-configuration-file"></a>Ajout d'un fichier de configuration de service
<a name="pj15_PrerequisitesWCF_AddConfig"> </a>

Si une application configure par programme les services WCF, elle n'utilise pas de fichier de configuration de service. Dans le cas contraire, une application Windows ou une application console utilise l'élément **System. ServiceModel** dans un fichier app. config; une application Web inclut **System. ServiceModel** dans Web. config. Pour plus d'informations sur l'utilisation d'un fichier app. config ou la configuration par programme des services WCF, voir [procédure pas à pas: développement d'applications PSI à l'aide de WCF](https://msdn.microsoft.com/library/65707234-c3da-44e4-8364-32a6be28f645%28Office.15%29.aspx).
  
Lorsqu'il génère un fichier source de proxy de service, la commande SvcUtil. exe crée également un fichier output. config qui sert de base à l'élément **System. ServiceModel** par défaut dans un fichier app. config ou Web. config. Le téléchargement du kit de développement logiciel (SDK) Project 2013 inclut `Documentation\IntelliSense\WCF\Source.zip`un exemple de fichier output. config dans. Par exemple, le fichier de sortie. config par défaut créé par SvcUtil. exe pour le service de ressources inclut deux liaisons nommées **BasicHttpBinding_Resource** et **BasicHttpBinding_Resource1**. L'élément **client** inclut deux points de terminaison par défaut. Un point de terminaison est pour l'accès sécurisé à l'adresse HTTP sur le port 32843 et l'autre à l'accès normal sur le port 32843, comme suit: 
  
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

La configuration du service PSI n'utilise pas les points de terminaison et les liaisons par défaut. Project Server exige que les applications accèdent aux services PSI via le serveur ProjectServer. svc frontal, qui agit comme un routeur pour les appels vers les services principaux. Pour créer le fichier app. config, procédez comme suit:
  
1. Si vous définissez une référence à l'assembly de proxy ProjectServerServices. dll ou que vous ajoutez le fichier source de proxy pour un service, l'application ne contient pas de fichier app. config. Ajoutez un nouvel élément au projet Visual Studio. Dans la boîte de dialogue **Ajouter un nouvel élément** , choisissez le modèle de **fichier de configuration** de l'application, nommez-le App. config, puis choisissez **Ajouter**.
    
2. Supprimez tout le texte du fichier app. config, puis copiez le code suivant dans le fichier. Vous pouvez utiliser la même liaison, par exemple `basicHttpConf`, pour chaque point de terminaison de service. Si vous souhaitez utiliser plusieurs liaisons, par exemple, pour lier les protocoles HTTP et HTTPs, vous devez créer une liaison pour chaque protocole.
    
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

3. Remplacez `ServerName/ProjectServerName` dans l'adresse du point de terminaison client par le nom de votre serveur et de votre instance Project Web App. 
    
4. Remplacez `ServiceName` par le nom du service PSI, tel que Resource. Assurez-vous de remplacer les trois instances du nom de service, par exemple:
    
    ```XML
        <endpoint address="https://myserver/pwa/_vti_bin/PSI/ProjectServer.svc"
            behaviorConfiguration="basicHttpBehavior" binding="basicHttpBinding"
            bindingConfiguration="basicHttpConf" 
            contract="SvcResource.Resource"
            name="basicHttp_Resource" />
    ```

5. Pour utiliser plusieurs services PSI, créez un élément de **point de terminaison** pour chaque service, et pour chaque élément de **liaison** utilisé par le service. Par exemple, les points de terminaison suivants configurent le client pour utiliser la liaison HTTP de base pour le service Project et le service QueueSystem. 
    
    > [!NOTE]
    > Si vous exécutez une application et obtenez une erreur indiquant que le serveur est trop occupé ou que la requête HTTP n'est pas autorisée, vérifiez que les adresses de point de terminaison sont correctes dans le fichier app. config. 
  
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

Vous pouvez modifier un fichier app. config à l'aide de l' **éditeur de configuration de service WCF** dans Visual Studio (dans le menu **Outils** ). La figure 4 montre comment définir l'élément **Contract** dans la boîte de dialogue **éditeur de configuration de service Microsoft** . Si la solution utilise l'assembly de proxy PSI, ouvrez ProjectServerServices. dll dans `bin\debug` le répertoire de la solution Visual Studio. La boîte de dialogue **type de contrat** affiche tous les contrats de service WCF (voir figure 5). 
  
**Figure 4. Utilisation de l'éditeur de configuration du service WCF**

![Utilisation de l'éditeur de configuration du service WCF] (media/pj15_PrerequisitesWCF_ServiceConfigurationEditor.gif "Utilisation de l'éditeur de configuration du service WCF")
  
Si la solution utilise un fichier proxy de service, tel que wcfResource.cs, compilez l'application, puis ouvrez le fichier exécutable dans `bin\debug` le répertoire. Pour plus d'informations sur la modification du fichier app. config, voir [procédure pas à pas: développement d'applications PSI à l'aide de WCF](https://msdn.microsoft.com/library/65707234-c3da-44e4-8364-32a6be28f645%28Office.15%29.aspx).
  
**Figure 5. Utilisation du navigateur de type de contrat dans l'éditeur de configuration du service WCF**

![Utilisation de l'Explorateur de types de contrat] (media/pj15_PrerequisitesWCF_ContractTypeBrowser.gif "Utilisation de l'Explorateur de types de contrat")
  
## <a name="using-multiple-authentication"></a>Utilisation de l'authentification multiple
<a name="pj15_PrerequisitesWCF_ClaimsMultiAuth"> </a>

L'authentification des utilisateurs Project Server locaux, qu'il s'agisse de l'authentification Windows ou de l'authentification par formulaires, est réalisée via le traitement des revendications dans SharePoint. L'authentification multiple signifie que l'application Web sur laquelle est configuré Project Web App prend en charge l'authentification Windows et l'authentification basée sur les formulaires. Si c'est le cas, tout appel à un service WCF qui utilise l'authentification Windows échouera avec l'erreur suivante, car le processus de revendications ne peut pas déterminer le type d'utilisateur à authentifier:
  
`The server was unable to process the request due to an internal error. For more information about the error, either turn on Include ExceptionDetailInFaults (either from ServiceBehaviorAttribute or from the <serviceDebug> configuration behavior) on the server in order to send the exception information back to the client, or turn on tracing as per the Microsoft .NET Framework 3.0 SDK documentation and inspect the server trace logs.`

Pour résoudre le problème pour WCF, tous les appels aux méthodes PSI doivent se trouver dans un **OperationContextScope** défini pour chaque service PSI. N'imbriquez pas les étendues pour plusieurs services; par exemple, lors de l'utilisation d'appels aux services de ressource et de projet, chaque ensemble d'appels doit se situer dans sa propre portée. 
  
Dans l'exemple suivant, la méthode **DisableFormsAuth** peut être appelée à partir de chaque section **OperationContextScope** dans une application. La méthode supprime toute valeur d'en-tête qui a précédemment désactivé l'authentification par formulaire, afin que l'authentification par formulaire puisse s'effectuer si le paramètre _isWindowsAuth_ est **false**. Si _isWindowsAuth_ a la **valeur true**, la méthode **DisableFormsAuth** désactive l'authentification par formulaire. 
  
Dans la méthode **WcfSample** , l'objet **ProjectClient** est une instance de la classe PSI **SvcProject. ProjectClient** . 
  
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
> Le fait d'appeler des appels PSI dans un **OperationContextScope** est requis uniquement pour les applications qui s'exécutent dans un environnement à plusieurs authentifications. Si Project Server utilise uniquement l'authentification Windows, il n'est pas nécessaire de définir une étendue et d'ajouter un en-tête de requête Web qui désactive l'authentification par formulaire. 
> 
> Le correctif pour une application basée sur ASMX est différent. Pour plus d'informations, reportez-vous à la section *utilisation de plusieurs authentifications* dans les [exemples de code basés sur ASMX dans Project](prerequisites-for-asmx-based-code-samples-in-project.md). 
  
## <a name="changing-values-of-generic-constants"></a>Modification des valeurs des constantes génériques
<a name="pj15_PrerequisitesWCF_ChangeValues"> </a>

La plupart des exemples contiennent une ou plusieurs variables que vous devez mettre à jour pour que l'exemple fonctionne correctement dans votre environnement. Dans l'exemple suivant, si SSL est installé, utilisez le protocole HTTPs au lieu du protocole HTTP. Remplacez _ServerName_ par le nom du serveur que vous utilisez. Remplacez _ProjectServerName_ par le nom du répertoire virtuel de votre site Project Server, par exemple, PWA. 
  
```cs
const string PROJECT_SERVER_URI = "https://ServerName/ProjectServerName/";
```

Toutes les autres variables que vous devez modifier sont indiquées en haut de l'exemple de code.
  
## <a name="verifying-the-results"></a>Vérification des résultats
<a name="pj15_PrerequisitesWCF_Verify"> </a>

L'obtention et l'interprétation de résultats à partir d'un exemple de code n'est pas toujours simple. Par exemple, si vous créez un projet, vous devez publier le projet avant de pouvoir l'afficher sur la page Centre de projets dans Project Web App.
  
Vous pouvez vérifier les résultats de l'exemple de code de plusieurs façons, par exemple:
  
- Utilisez le client Project Professional 2013 pour ouvrir le projet à partir de l'ordinateur Project Server et afficher les éléments de votre choix.
    
- Affichez les projets publiés sur la page Centre de projets de Project `https://ServerName/ProjectServerName/projects.aspx`Web App ().
    
- Affichez le journal de la file d'attente dans Project Web App. Ouvrez la page Paramètres du serveur (cliquez sur l'icône **paramètres** dans le coin supérieur droit), puis choisissez **mes travaux en file d'attente** sous la section **paramètres personnels** ( `https://ServerName/ProjectServerName/MyJobs.aspx`). Dans la liste déroulante **affichage** , vous pouvez trier en fonction de l'état du travail. L'État par défaut est **en cours et échecs de travaux au cours de la semaine précédente**. 
    
- Utilisez la page Paramètres du serveur dans Project Web App `https://ServerName/ProjectServerName/_layouts/15/pwa/admin/admin.aspx`() pour gérer tous les travaux en file d'attente et supprimer ou forcer l'archivage des objets d'entreprise. Vous devez disposer d'autorisations d'administration pour accéder à ces liens sur la page Paramètres du serveur.
    
- Utilisez **Microsoft SQL Server Management Studio** pour exécuter une requête sur une table d'une base de données Project Server. Par exemple, utilisez la requête suivante pour sélectionner les 200 premières lignes du tableau MSP_WORKFLOW_STAGE_PDPS pour afficher des informations sur les pages de détails de projet (PDP) dans les étapes du flux de travail. 
    
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

Une fois que vous avez testé certains exemples de code, il existe des objets d'entreprise et des paramètres qui doivent être supprimés ou réinitialisés. Vous pouvez utiliser la page Paramètres du serveur dans Project Web App pour gérer les données `https://ServerName/ProjectServerName/_layouts/15/pwa/admin/admin.aspx`d'entreprise (). Les liens de la page Paramètres du serveur vous permettent de supprimer les anciens éléments, de forcer l'archivage des projets, de gérer la file d'attente des travaux pour tous les utilisateurs et d'effectuer d'autres tâches d'administration.
  
Voici quelques-uns des liens figurant sur la page Paramètres du serveur à utiliser pour les activités de nettoyage classiques après l'exécution d'exemples de code:
  
- **Champs personnalisés d’entreprise et tables de choix**
    
- **Gérer les travaux en file d’attente**
    
- **Supprimer des objets d’entreprise**
    
- **Forcer l'archivage des objets d'entreprise**
    
- **Types de projets d’entreprise**
    
- **Phases du flux de travail**
    
- **Étapes du flux de travail**
    
- **Pages de détails de projet**
    
- **Périodes de rapports de temps**
    
- **Paramètres et valeurs par défaut de la feuille de temps**
    
- **Classifications de ligne**
    
Les paramètres supplémentaires sont gérés par SharePoint Server 2013 pour chaque instance Project Web App, et non par une page de paramètres de serveur Project Web App spécifique. Dans l'application Administration centrale de SharePoint, choisissez **paramètres généraux**de l'application, choisissez **gérer** sous **paramètres de Project Server**, puis choisissez l'instance de Project Web App dans la liste déroulante de la page Paramètres du serveur. . Par exemple, choisissez **gestionnaires d'événements côté serveur** pour ajouter ou supprimer des gestionnaires d'événements pour l'instance Project Web App sélectionnée. 
  
## <a name="see-also"></a>Voir aussi

- [Conditions préalables pour les exemples de code basés sur ASMX](prerequisites-for-asmx-based-code-samples-in-project.md)   
- [Procédure pas à pas: développement d'applications PSI à l'aide de WCF](https://msdn.microsoft.com/library/65707234-c3da-44e4-8364-32a6be28f645%28Office.15%29.aspx)   
- [Utiliser l'emprunt d'identité avec WCF](https://msdn.microsoft.com/library/e3597901-2f02-44a2-8076-d32aae540b38%28Office.15%29.aspx)  
- [Vue d’ensemble de la référence Project PSI](project-psi-reference-overview.md) 
- [Centre pour développeurs SharePoint](https://msdn.microsoft.com/sharepoint/default.aspx)
    

