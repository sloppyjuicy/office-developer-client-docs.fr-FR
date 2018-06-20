---
title: Conditions techniques
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: overview
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: eff6d5d6-8855-4e54-a781-9deab8cc0aca
description: Cette rubrique décrit les langages de programmation pris en charge, la méthode et la visibilité COM renvoient des exigences de type et les détails de l’extensibilité de fournisseur Outlook Social Connector (OSC) DLL.
ms.openlocfilehash: 94b57e20957f3d8d779c4d3324ecbb8ccd37f60a
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19787706"
---
# <a name="technical-requirements"></a>Conditions techniques

Cette rubrique décrit les langages de programmation pris en charge, la méthode et la visibilité COM renvoient des exigences de type et les détails de l’extensibilité de fournisseur Outlook Social Connector (OSC) DLL. 
  
## <a name="programming-language-and-com-requirements"></a>Langage de programmation en matière de COM

Vous pouvez créer un fournisseur OSC à l’aide des langages managés tels que Visual c# ou Visual Basic ou langages non managés tels que Visual C++. Vous pouvez utiliser n’importe quel outil que vous pouvez créer un composant DLL COM visibles pour développer un fournisseur OSC. La décision d’utiliser un langage managé ou non managé pour développer un fournisseur doit prendre en compte la taille de téléchargement et les dépendances du package d’installation fournisseur.
  
Un fournisseur OSC doit être visible par COM, tel que défini par les éléments suivants :
  
- Après l’installation, un fournisseur OSC doit être enregistré à l’aide de l’inscription automatique COM ou regsvr32.
    
- Un enregistrement d’un fournisseur OSC DLL COM enregistre le fournisseur dans HKCU ou HKLM. 
    
- ProgID d’un fournisseur est enregistré sous `HKCU\Software\Microsoft\Office\Outlook\SocialConnector\SocialProviders`.
    
- Un fournisseur OSC développé dans un langage managé est visible par COM.
    
- Un fournisseur OSC doit ajouter les valeurs dans le Registre Windows qui indiquent que la DLL du fournisseur prend en charge un seul thread cloisonné et apartment multithread (MTA) modèles de thread. Pour plus d’informations sur les modèles de thread COM, voir [Descriptions et fonctionnement de OLE modèles de thread](http://support.microsoft.com/kb/150777).
    
Méthodes de l’extensibilité de fournisseur OSC doivent retourner types primitifs comme **chaîne** ou **bool**. Certains **chaîne** renvoie les valeurs doivent être conformes à la définition de schéma pour l’extensibilité de fournisseur OSC. XML uniquement est pris en charge en tant que valeur de retour. 
  
## <a name="details-of-the-osc-provider-extensibility-dll"></a>Détails de l’extensibilité de fournisseur OSC DLL

Le composant qui prend en charge l’extensibilité de fournisseur OSC est l’extensibilité du fournisseur OSC DLL. Les développeurs tiers peuvent créer des DLL de fournisseur OSC à l’aide de ces interfaces d’extensibilité. La liste suivante présente les détails de l’extensibilité de fournisseur OSC DLL :
  
- Nom du fichier DLL extensibilité : socialprovider.dll
    
- Nom convivial de la DLL de l’extensibilité : extensibilité de fournisseur Social Microsoft Outlook
    
- Version principale de l’extensibilité DLL : 15.0
    
- Version de bibliothèque de types de DLL Extensibiilty : 1.1
    
## <a name="miscellaneous-technical-information"></a>Informations techniques diverses

JavaScript Object Notation (JSON) n’est pas pris en charge dans le modèle d’extensibilité de fournisseur OSC.
  
Il n’existe aucune dépendance sur un analyseur XML. Le fournisseur OSC permettre utiliser un analyseur XML qui est inclus avec Office, telles que Microsoft XML Core Services (MSXML), utilisez le code XML l’analyse des fonctionnalités intégrées à Microsoft .NET Framework ou un analyseur XML de tiers. 
  
## <a name="see-also"></a>Voir aussi

- [Meilleures pratiques pour le développement d’un fournisseur](best-practices-for-developing-a-provider.md)  
- [Étapes rapides pour apprendre à développer un fournisseur](quick-steps-for-learning-to-develop-a-provider.md)
- [Déploiement d'un fournisseur](deploying-a-provider.md)  
- [Prise en main du développement d'un fournisseur Outlook Social Connector](getting-started-with-developing-an-outlook-social-connector-provider.md)

