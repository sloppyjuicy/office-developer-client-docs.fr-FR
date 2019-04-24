---
title: Exigences techniques
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: overview
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: eff6d5d6-8855-4e54-a781-9deab8cc0aca
description: Cette rubrique décrit les langages de programmation pris en charge, la visibilité COM et les conditions requises pour le type de retour de la méthode, ainsi que les détails de la DLL d'extensibilité du fournisseur Outlook Social Connector (OSC).
ms.openlocfilehash: 14dfcf52d714177775c5610b5da91d174f81a132
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32329154"
---
# <a name="technical-requirements"></a>Exigences techniques

Cette rubrique décrit les langages de programmation pris en charge, la visibilité COM et les conditions requises pour le type de retour de la méthode, ainsi que les détails de la DLL d'extensibilité du fournisseur Outlook Social Connector (OSC). 
  
## <a name="programming-language-and-com-requirements"></a>Configuration requise pour le langage de programmation et COM

Vous pouvez créer un fournisseur OSC en utilisant des langages managés, tels que Visual C# ou Visual Basic, ou des langages non managés, tels que Visual C++. Vous pouvez utiliser n'importe quel outil capable de créer un composant DLL visible par COM pour développer un fournisseur OSC. La décision d'utiliser un langage managé ou non managé pour développer un fournisseur doit prendre en compte la taille de téléchargement et les dépendances du package d'installation du fournisseur.
  
Un fournisseur OSC doit être visible par COM, comme défini par les éléments suivants:
  
- Après l'installation, un fournisseur OSC doit être enregistré à l'aide de l'auto-enregistrement COM ou de regsvr32.
    
- L'inscription COM d'une DLL de fournisseur OSC inscrit le fournisseur sous HKCU ou HKLM. 
    
- Le ProgID d'un fournisseur est enregistré `HKCU\Software\Microsoft\Office\Outlook\SocialConnector\SocialProviders`sous.
    
- Un fournisseur OSC développé dans un langage managé est visible par COM.
    
- Un fournisseur OSC doit ajouter des valeurs au registre Windows qui indiquent que la DLL du fournisseur prend en charge les modèles de thread cloisonné (STA) et multithread (MTA). Pour plus d'informations sur les modèles de thread COM, voir [descriptions and workings of OLE threadIng Models](https://support.microsoft.com/kb/150777).
    
Les méthodes de l'extensibilité du fournisseur OSC doivent retourner des types primitifs, tels que **String** ou **bool**. Certaines valeurs de retour de **chaîne** doivent être conformes à la définition de schéma pour l'extensibilité du fournisseur OSC. Seul XML est pris en charge en tant que valeur de retour. 
  
## <a name="details-of-the-osc-provider-extensibility-dll"></a>Détails de la DLL d'extensibilité du fournisseur OSC

Le composant qui prend en charge l'extensibilité du fournisseur OSC est la DLL d'extensibilité du fournisseur OSC. Les développeurs tiers peuvent créer des dll de fournisseur OSC à l'aide de ces interfaces d'extensibilité. La liste suivante indique les détails de la DLL d'extensibilité du fournisseur OSC:
  
- Nom du fichier DLL d'extensibilité: socialprovider. dll
    
- Nom convivial de la DLL d'extensibilité: extensibilité des fournisseurs de réseaux sociaux Microsoft Outlook
    
- Version principale de la DLL d'extensibilité: 15,0
    
- Extensibiilty DLL TypeLib version: 1,1
    
## <a name="miscellaneous-technical-information"></a>Informations techniques diverses

JavaScript Object Notation (JSON) n'est pas pris en charge dans le modèle d'extensibilité du fournisseur OSC.
  
Il n'existe aucune dépendance vis-à-vis d'un analyseur XML. Le fournisseur OSC peut utiliser un analyseur XML inclus dans Office, comme Microsoft XML Core Services (MSXML), utiliser les fonctionnalités d'analyse XML intégrées à Microsoft .NET Framework ou utiliser un analyseur XML tiers. 
  
## <a name="see-also"></a>Voir aussi

- [Meilleures pratiques pour le développement d'un fournisseur](best-practices-for-developing-a-provider.md)  
- [Étapes rapides pour apprendre à développer un fournisseur](quick-steps-for-learning-to-develop-a-provider.md)
- [Déploiement d'un fournisseur](deploying-a-provider.md)  
- [Prise en main du développement d'un fournisseur Outlook Social Connector](getting-started-with-developing-an-outlook-social-connector-provider.md)

