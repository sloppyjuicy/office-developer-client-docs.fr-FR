---
title: Développement de modèles de formulaires à l’aide du modèle objet InfoPath 2003
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
keywords:
- form templates [infopath 2007], using infopath 2003 object model,InfoPath 2003-compatible form templates,InfoPath 2007, developing form templates using InfoPath 2003 object model,object models [InfoPath 2003], developing managed code form templates
localization_priority: Normal
ms.assetid: c74cbcd0-4fe6-4eb7-a05c-f61e1868c42b
description: Microsoft InfoPath prend toujours en charge les projets de modèle de formulaires créés avec Microsoft Office InfoPath 2003 Toolkit pour Visual Studio .NET ou Visual Studio 2005 Tools pour Microsoft Office et dont la logique métier a été écrite en fonction des membres de l'espace de noms Microsoft.Office.Interop.InfoPath.SemiTrust . Les rubriques de cette section désignent les types et les membres de cet espace de nom par modèle objet compatible InfoPath 2003 ou simplement par modèle objet InfoPath 2003. InfoPath prend également en charge les projets de modèle de formulaire créés avec Microsoft Office InfoPath 2007, qui utilisent le modèle objet compatible avec InfoPath 2003. Par ailleurs, à l'aide de InfoPath, vous pouvez créer des projets de modèle de formulaire intégrant un modèle objet compatible avec InfoPath 2003 afin de préserver la rétrocompatibilité pour les utilisateurs de Office InfoPath 2007. Toutes les rubriques de cette section traitent de la création et du développement de modèles de formulaires utilisant le modèle objet compatible avec InfoPath 2003 fourni par l'espace de noms Microsoft.Office.Interop.InfoPath.SemiTrust .
ms.openlocfilehash: a39f921f6c7465dbcf469062b866c808fa222851
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32300363"
---
# <a name="developing-form-templates-using-the-infopath-2003-object-model"></a>Développement de modèles de formulaires à l’aide du modèle objet InfoPath 2003

Microsoft InfoPath prend toujours en charge les projets de modèle de formulaires créés avec Microsoft Office InfoPath 2003 Toolkit pour Visual Studio .NET ou Visual Studio 2005 Tools pour Microsoft Office et dont la logique métier a été écrite en fonction des membres de l'espace de noms [Microsoft.Office.Interop.InfoPath.SemiTrust](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust.aspx) . Les rubriques de cette section désignent les types et les membres de cet espace de nom par modèle objet compatible InfoPath 2003 ou simplement par modèle objet InfoPath 2003. InfoPath prend également en charge les projets de modèle de formulaire créés avec Microsoft Office InfoPath 2007, qui utilisent le modèle objet compatible avec InfoPath 2003. Par ailleurs, à l'aide de InfoPath, vous pouvez créer des projets de modèle de formulaire intégrant un modèle objet compatible avec InfoPath 2003 afin de préserver la rétrocompatibilité pour les utilisateurs de Office InfoPath 2007. Toutes les rubriques de cette section traitent de la création et du développement de modèles de formulaires utilisant le modèle objet compatible avec InfoPath 2003 fourni par l'espace de noms [Microsoft.Office.Interop.InfoPath.SemiTrust](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust.aspx) . 
  
> [!IMPORTANT]
> [!IMPORTANTE] Même si la création d'une logique métier à l'aide du modèle objet avec code managé fourni par l'espace de noms [Microsoft.Office.Interop.InfoPath.SemiTrust](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust.aspx) est toujours prise en charge par InfoPath, la logique écrite avec ce modèle objet n'est pas prise en charge pour les modèles de formulaires activés pour le navigateur déployés dans Microsoft SharePoint Server 2010 avec InfoPath Forms Services. Les modèles de formulaires activés pour le navigateur doivent utiliser le nouveau modèle objet InfoPath avec code managé fourni par l'espace de noms [Microsoft.Office.InfoPath](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.aspx) pour une logique métier personnalisée. Pour plus d'informations sur la création de modèles de formulaires avec une logique métier utilisant des membres de l'espace de noms [Microsoft.Office.InfoPath](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.aspx) , voir [Développement de modèles de formulaire InfoPath avec code](developing-infopath-form-templates-with-code.md). > Notez également que les utilisateurs de modèles de formulaires compilés avec Visual Studio 2012 doivent avoir installé Microsoft .NET Framework 2.0 ou version ultérieure sur leur ordinateur. Les utilisateurs de modèles de formulaires compilés avec Visual Studio .NET 2003 n'ont besoin que de Microsoft .NET Framework 1.1 sur leur ordinateur. 
  
## <a name="in-this-section"></a>Contenu de cette section

[Mise en place du développement de modèles de formulaires à l’aide du modèle objet InfoPath 2003](get-started-developing-form-templates-using-infopath-object-model.md)
  
> Fournit des informations sur la marche à suivre pour se lancer dans la création de modèles de formulaires avec code managé fonctionnant avec le modèle objet compatible avec InfoPath 2003.
    
[Création de modèles de formulaires à l’aide du modèle objet InfoPath 2003](creating-form-templates-using-the-infopath-2003-object-model.md)
  
> Cette section présente le code d'initialisation et de nettoyage, l'ajout de gestionnaires d'événements, le débogage et le déploiement des modèles de formulaires InfoPath avec code managé, la gestion des threads et l'utilisation de MSXML à partir de solutions InfoPath avec code managé.
    
[Sécurité dans les modèles de formulaire InfoPath avec code](security-in-infopath-form-templates-with-code.md)
  
> Présente le modèle de sécurité des modèles de formulaires InfoPath avec code managé, le débogage des modèles de formulaires InfoPath entièrement fiables, ainsi que les procédures de sécurité associées.
    
[Présentation du modèle objet InfoPath 2003](understanding-the-infopath-2003-object-model.md)
  
> Présente le modèle objet compatible avec InfoPath 2003, ainsi que les tâches de programmation courantes dans le cas des modèles de formulaires avec code managé fonctionnant avec ce modèle objet.
    
[Dépannage des modèles de formulaire qui utilisent le modèle objet InfoPath 2003](troubleshoot-form-templates-that-use-infopath-object-model.md)
  
> Cette section contient des astuces permettant de résoudre des problèmes que vous pouvez rencontrer lors de la création de modèles de formulaires avec code managé fonctionnant avec le modèle objet compatible avec InfoPath 2003.
    
## <a name="related-sections"></a>Sections connexes

[Portail des développeurs InfoPath (éventuellement en anglais)](https://go.microsoft.com/fwlink?LinkID=11689)
  
> Contient des liens vers des articles techniques, des exemples de code, des téléchargements et d'autres documents MSDN (Microsoft Developer Network) sur la création de solutions InfoPath personnalisées.
    
[Centre pour développeurs Office](https://go.microsoft.com/fwlink?LinkID=27128)
  
> Contient des liens vers des articles techniques, des exemples de code, des téléchargements et d'autres documents MSDN (Microsoft Developer Network) sur la création de solutions Office personnalisées.
    

