---
title: Modèles objet et environnement de développement d'InfoPath
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
keywords:
- infopath 2007, object models,object models [InfoPath 2007],InfoPath 2007, development environments
localization_priority: Normal
ms.assetid: 29415c5b-9a42-46f4-a9e8-6a7d5bb7bdbf
description: Microsoft InfoPath 2013 prend en charge deux types de modèles de programmation pour le développement d’une logique métier dans les modèles de formulaire et prend en charge l’automatisation externe à partir du code managé.
ms.openlocfilehash: c2ed1254acf86136ab7144c732aef91ac4c14c53
ms.sourcegitcommit: ef717c65d8dd41ababffb01eafc443c79950aed4
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 10/04/2018
ms.locfileid: "25400109"
---
# <a name="understanding-infopath-object-models-and-development-environment"></a>Présentation des modèles objet InfoPath et de l’environnement de développement

Microsoft InfoPath 2013 prend en charge deux types de modèles de programmation pour le développement d’une logique métier dans les modèles de formulaire et prend en charge l’automatisation externe à partir du code managé.
  
InfoPath Forms Services, qui est disponible dans SharePoint Server 2013, fournit une expérience de navigation Web pour remplir les formulaires InfoPath. Lors du déploiement sur un serveur qui exécute InfoPath Forms Services, des formulaires basés sur des formulaires compatibles avec le navigateur modèles (.xsn) peuvent être ouvert dans un navigateur Web sur les ordinateurs qui ne disposent pas d’InfoPath, mais ils seront ouvre dans InfoPath lorsqu’il est installé. InfoPath Forms Services fournit également un modèle objet pour l’automatisation des tâches de serveur relatifs à l’administration et la publication du modèle de formulaire InfoPath.
  
InfoPath 2013 prend en charge le Visual Studio 2012 de programmation environnement et ses langages de programmation associés, qui sont décrites plus loin dans cette rubrique.
  
## <a name="infopath-programming-models"></a>Modèles de programmation InfoPath

InfoPath 2013 prend en charge deux modèles d’objet pour le développement d’une logique métier dans les modèles de formulaire :
  
- le modèle objet avec code managé InfoPath ;
    
- le modèle objet avec code managé compatible avec InfoPath 2003.
    
En outre, InfoPath 2013 permet d’écrire du code managé automatiser InfoPath à partir d’une application externe.
  
InfoPath Forms Services fournit un modèle objet qui permet l'automatisation des tâches de serveur, telles que la vérification et le téléchargement de modèles de formulaires à partir de code s'exécutant sur le serveur, ce qui nécessite un accès et des autorisations d'administrateur de serveur.
  
> [!NOTE]
> Le InfoPath Filler 2013 ouvrir et exécuter des solutions de modèle créées dans les versions antérieures d’InfoPath qui utilisent une logique métier écrite avec des langages de script (JScript et VBScript) de formulaire InfoPath. Cependant, InfoPath Designer 2010 ne prend pas en charge la création ou la modification de modèles de formulaire utilisant une logique métier écrite à l'aide d'un script. 
  
### <a name="the-infopath-managed-code-object-model"></a>Modèle objet InfoPath avec code managé

Le modèle objet de code managé InfoPath 2013 est implémenté dans deux assemblys qui sont nommés Microsoft.Office.Infopath.dll.
  
Une version de l’assembly implémente un sous-ensemble du modèle objet InfoPath qui contient uniquement les types et membres qui sont pris en charge dans la logique métier des modèles de formulaire déployés en tant que les modèles de formulaires activés pour le navigateur en cours d’exécution sur SharePoint Server 2013 avec InfoPath Forms Services. Les modèles de formulaires associés à une logique métier écrite en prenant en compte cet assembly peuvent être ouverts et exécutés dans InfoPath Filler et dans un navigateur Web.
  
L'autre version de l'assembly implémente des types et membres supplémentaires qui offrent des fonctions non prises en charge dans la logique métier des modèles de formulaires compatibles avec le navigateur. Les modèles de formulaires associés à une logique métier écrite en prenant en compte les classes et membres supplémentaires de cet assembly s'ouvrent et s'exécutent uniquement dans l'éditeur InfoPath Filler.
  
> [!NOTE]
> [!REMARQUE] Il est possible d'écrire une logique conditionnelle qui utilise les propriétés de la classe [Environment](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.Environment.aspx) pour déterminer dans quel environnement (InfoPath Filler ou un navigateur Web) le modèle de formulaire s'exécute. Grâce à cette logique conditionnelle, votre logique métier peut alterner entre du code fonctionnant dans un navigateur Web et du code écrit en fonction des classes et des membres fonctionnant uniquement dans l'éditeur InfoPath Filler. Pour plus d’informations, consultez la rubrique [écrire une logique conditionnelle qui détermine l’environnement d’exécution](how-to-write-conditional-logic-that-determines-the-run-time-environment.md)
  
L'assembly utilisé par InfoPath lorsque vous ajoutez et compilez une logique métier pour le modèle de formulaire varie selon que vous sélectionnez le modèle de formulaire **Formulaire vierge** ou le modèle de formulaire **Formulaire vierge (InfoPath Filler)** dans l'onglet **Nouveau** de Microsoft Office Backstage lorsque vous commencez à créer un nouveau formulaire dans InfoPath Designer. Les formulaires créés en utilisant le modèle de formulaire **Formulaire vierge** utilisent l'assembly qui contient uniquement les types et membres pris en charge dans la logique métier des modèles de formulaires déployés en tant que modèles de formulaires compatibles avec le navigateur. Les formulaires créés à l'aide du modèle de formulaire **Formulaire vierge** peuvent être ouverts dans le navigateur Web et dans InfoPath Filler. Les formulaires créés à l'aide du modèle de formulaire **Formulaire vierge (InfoPath Filler)** utilisent l'assembly implémentant les types et membres supplémentaires qui offrent des fonctions non prises en charge dans la logique métier des modèles de formulaires compatibles avec le navigateur. Ils doivent uniquement être ouverts dans InfoPath Filler. 
  
> [!TIP]
> Une fois que vous commencez à concevoir un modèle de formulaire, vous pouvez modifier l’assembly est utilisé en modifiant les paramètres de compatibilité du formulaire. Pour ce faire, cliquez sur **Langage** dans l'onglet **Développeur**, puis cliquez sur **Compatibilité** dans la liste **Catégorie**. Dans la liste **type de formulaire** , sélectionnez **Formulaires de navigateur Web** pour créer un formulaire qui peut être déployé comme un formulaire compatible avec le navigateur sur SharePoint Server 2013. Sélectionnez **Formulaire InfoPath Filler** pour créer un formulaire qui pourra uniquement être exécuté dans l'éditeur InfoPath Filler. Les autres options disponibles dans la liste **Type de formulaire** permettent d'assurer la compatibilité avec InfoPath 2007 et InfoPath 2003. 
  
Les classes et les membres des deux versions de ce modèle objet sont exposés via l'espace de noms [Microsoft.Office.InfoPath](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.aspx) . Le tableau suivant répertorie les où les assemblys sont trouvent dans les répertoires d’une installation d’InfoPath 2013. 
  
|**Assembly**|**Description**|
|:-----|:-----|
|Microsoft.Office.InfoPath.dll (dans C:\Program Files\Microsoft Office\Office15\InfoPathOM\InfoPathOMFormServices)  <br/> |Le sous-ensemble du modèle d’objet qui contient uniquement les types et membres qui s’exécuteront dans la logique métier d’un modèle de formulaire déployé sur un serveur exécutant InfoPath Forms Services.  <br/> |
|Microsoft.Office.InfoPath.dll (dans C:\Program Files\Microsoft Office\Office15\InfoPathOM)  <br/> |Le modèle objet « complet », y compris des types et des membres qui s’exécuteront pas dans la logique métier d’un modèle de formulaire déployé dans InfoPath Forms Services.  <br/> |
   
> [!NOTE]
> [!REMARQUE] Les assemblys mentionnés plus haut sont utilisés en phase de création lors de l'écriture et de la compilation de code. Pendant l'exécution, l'assembly utilisé lors de l'ouverture d'un modèle de formulaire dans InfoPath réside dans le GAC (Global Assembly Cache) de l'ordinateur sur lequel InfoPath est installé. Lorsqu'un modèle de formulaire est ouvert dans un navigateur Web à partir d'un serveur exécutant InfoPath Forms Services, l'assembly utilisé réside sur le serveur. 
  
En disposant de deux assemblys, vous avez l'assurance que votre logique métier contiendra uniquement des appels aux membres du modèle objet adaptés aux éditeurs de code de formulaire pris en charge (navigateur Web ou InfoPath Filler). Par exemple, lorsque vous éditez votre code, les fonctions IntelliSense de saisie semi-automatique et de documentation en ligne s'afficheront et fonctionneront uniquement pour les membres du modèle objet adaptés à vos éditeurs de formulaires cibles.
  
Dans les deux versions du modèle objet avec code managé exposé par l'assembly Microsoft.Office.InfoPath, la consultation et la mise à jour des magasins de données XML d'une logique métier nécessitent des appels aux membres de la classe **System.Xml.XPath.XPathNavigator**. Dans InfoPath 2003, la consultation et la mise à jour des magasins de données XML nécessitent l'appel aux membres de classes MSXML (pour une logique métier créée à l'aide de JScript ou VBScript) ou un appel via les wrappers des classes MSXML fournies par l'espace de noms **Microsoft.Office.Interop.InfoPath.SemiTrust** (pour une logique métier créée à l'aide de C# ou Visual Basic et Microsoft Office InfoPath 2003 Toolkit pour Visual Studio .NET). 
  
À l’aide des membres de la classe **XPathNavigator** permet le même code de logique métier prendre en charge la manipulation du modèle DOM des modèles de formulaires ouverts dans le client InfoPath et dans les formulaires Web ouverts à partir de SharePoint Server 2013 avec des formulaires InfoPath Services dans un navigateur Web. 
  
Pour plus d’informations sur l’utilisation des membres de la classe **XPathNavigator** dans la logique métier d’InfoPath modèles de formulaires avec code managé, voir [utiliser les Classes XPathNavigator et XPathNodeIterator](how-to-work-with-the-xpathnavigator-and-xpathnodeiterator-classes.md).
  
### <a name="the-infopath-2003-compatible-managed-code-object-model"></a>Modèle objet avec code managé compatible avec InfoPath 2003

Le modèle objet avec code managé compatible avec InfoPath 2003 a été inauguré dans InfoPath 2003 Service Pack 1 en même temps que Microsoft Office InfoPath 2003 Toolkit pour Visual Studio .NET pour permettre la création d'une logique métier dans les modèles de formulaires avec code managé. Ce modèle d’objet est toujours pris en charge par InfoPath 2013 pour assurer la compatibilité avec InfoPath 2003.
  
Les classes et les membres de ce modèle objet sont exposés via l'espace de noms [Microsoft.Office.Interop.InfoPath.SemiTrust](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust.aspx) . Ce modèle d’objet est implémenté dans le fichier d’assembly suivantes qui se trouve dans le dossier C:\Program Files\Microsoft Office\Office14. 
  
|**Assembly**|**Description**|
|:-----|:-----|
|Microsoft.Office.Interop.InfoPath.SemiTrust.dll  <br/> |Fournit une interopérabilité COM par rapport au modèle d’objet COM d’InfoPath pour un formulaire modèle la logique métier écrite à l’aide de c# ou Visual Basic.  <br/> |
   
> [!NOTE]
> Bien que la création d’une logique métier avec le modèle d’objet de code managé interopérabilité COM fourni par l’assembly Microsoft.Office.Interop.InfoPath.SemiTrust est toujours pris en charge par InfoPath 2013, la logique métier écrite à l’aide de ce modèle d’objet pour que n’est pas pris en charge modèles de formulaire activés pour le navigateur déployés vers SharePoint Server 2013 avec InfoPath Forms Services. Les modèles de formulaires compatibles avec le navigateur doivent utiliser le modèle objet InfoPath avec code managé dans le cas d'une logique métier personnalisée. 
  
### <a name="automating-infopath-from-managed-code"></a>Automatisation d'InfoPath à partir de code managé

En plus de pouvoir écrire une logique métier avec du code managé, les développeurs peuvent également automatiser InfoPath au moyen de code managé s'exécutant dans une application externe. Cette fonctionnalité et les assemblys requis pour l'écriture de code ont été introduits dans InfoPath 2003 Service Pack 1. Les objets et les membres pour l’automatisation d’InfoPath ont été mis à jour pour fournir des fonctionnalités supplémentaires lorsque vous écrivez du code d’automatisation externe pour InfoPath 2013.
  
Les classes et les membres utilisés pour l'automatisation externe sont exposés via les espaces de noms [Microsoft.Office.Interop.InfoPath](https://msdn.microsoft.com/library/microsoft.office.interop.infopath.aspx) et [Microsoft.Office.Interop.InfoPath.Xml](https://msdn.microsoft.com/library/microsoft.office.interop.infopath.xml). Les fichiers d’assembly qui sont nécessaires pour l’écriture de code d’automatisation se trouvent dans le dossier C:\Program Files\Microsoft Office\Office14. 
  
|**Assembly**|**Description**|
|:-----|:-----|
|Microsoft.Office.Interop.InfoPath.dll  <br/> |Fournit une interopérabilité COM par rapport au modèle d’objet COM d’InfoPath pour le code d’automatisation externe écrit à l’aide de c# ou Visual Basic.  <br/> |
|Microsoft.Office.Interop.InfoPath.Xml.dll  <br/> |Fournit une interopérabilité COM par rapport à l’analyseur MSXML pour les opérations DOM XML contenues dans le code d’automatisation externe écrit à l’aide de C# ou de Visual Basic.  <br/> |
   
Pour plus d’informations sur les modèles objet fourni par les espaces de noms **Microsoft.Office.Interop.InfoPath** et **Microsoft.Office.Interop.InfoPath.Xml** , qui sont utilisés exclusivement pour automatiser l’application InfoPath à l’aide de gérés code à partir d’applications externes, consultez le [Centre pour développeurs InfoPath](https://msdn.microsoft.com/office/aa905434.aspx).
  
### <a name="the-infopath-forms-services-object-model"></a>Modèle objet InfoPath Forms Services

Le modèle objet de code managé pour l’automatisation des tâches d’administration InfoPath Forms Services est implémenté dans le Microsoft.Office.InfoPath.Server.dll qui se trouve dans \<lecteur\>: \Program Files\Microsoft Server\15.0\Bin Office sur un Installation de Microsoft SharePoint Server 2013.
  
|**Assembly**|**Description**|
|:-----|:-----|
|Microsoft.Office.InfoPath.Server.dll  <br/> |Le modèle objet pour l’automatisation des tâches InfoPath Forms Services tels que le téléchargement, l’activation ou désactivation des modèles de formulaires activés pour le navigateur.  <br/> |
   
Pour plus d’informations sur le modèle objet InfoPath Forms Services, voir le SharePoint Server 2013 logiciel les développeurs Kit (SDK) qui est disponible sur MSDN.
  
## <a name="infopath-development-environment"></a>Environnement de développement InfoPath

Le développement d’une logique métier dans les modèles de formulaires InfoPath 2013 peut être effectué à l’aide de Visual Studio 2012 avec le module complémentaire [Microsoft Visual Studio Tools pour Applications 2012](https://www.microsoft.com/en-us/download/details.aspx?id=38807) installé. 
  
> [!NOTE]
> InfoPath 2013 ne prend pas en charge la création ou modification des modèles de formulaires qui utilisent une logique métier écrite avec JScript ou VBScript, bien que InfoPath Filler prend en charge les modèles de formulaire basé sur un script d’ouverture qui ont été créés dans les versions précédentes d’InfoPath. 
  
## <a name="see-also"></a>Voir aussi

- [Procédure : Création d’un modèle de formulaire de base avec code](walkthrough-creating-a-basic-form-template-with-code.md)
- [Procédure pas à pas : Création et débogage d'un modèle de formulaire basique à l'aide du modèle objet InfoPath 2003](walkthrough-create-and-debug-basic-form-template-using-infopath-object-model.md)

