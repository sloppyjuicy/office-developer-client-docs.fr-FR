---
title: Exigences techniques
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: overview
ms.prod: office-online-server
ms.localizationpriority: medium
ms.assetid: eff6d5d6-8855-4e54-a781-9deab8cc0aca
description: Cette rubrique décrit les langages de programmation pris en charge, la visibilité COM et les exigences de type de retour de méthode, ainsi que les détails de la DLL d’extensibilité du fournisseur OSC (Outlook Social Connector).
ms.openlocfilehash: 5d5ca78c7ff1e328257b7e645731e76a2e6e5633
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/24/2021
ms.locfileid: "59604059"
---
# <a name="technical-requirements"></a>Exigences techniques

Cette rubrique décrit les langages de programmation pris en charge, la visibilité COM et les exigences de type de retour de méthode, ainsi que les détails de la DLL d’extensibilité du fournisseur OSC (Outlook Social Connector). 
  
## <a name="programming-language-and-com-requirements"></a>Langage de programmation et exigences COM

Vous pouvez créer un fournisseur OSC à l’aide de langages gérés tels que Visual C# ou Visual Basic, ou de langages non gérés tels que Visual C++. Vous pouvez utiliser n’importe quel outil qui peut créer un composant DLL visible par COM pour développer un fournisseur OSC. La décision d’utiliser une langue gérée ou non gérée pour développer un fournisseur doit prendre en compte la taille de téléchargement et les dépendances du package d’installation du fournisseur.
  
Un fournisseur OSC doit être visible par COM comme défini par les suivants :
  
- Après l’installation, un fournisseur OSC doit être inscrit à l’aide de l’auto-inscription COM ou de regsvr32.
    
- L’inscription COM d’une DLL de fournisseur OSC inscrit le fournisseur sous HKCU ou HKLM. 
    
- ProgID d’un fournisseur est inscrit sous  `HKCU\Software\Microsoft\Office\Outlook\SocialConnector\SocialProviders` .
    
- Un fournisseur OSC développé dans un langage géré est visible par COM.
    
- Un fournisseur OSC doit ajouter au Registre Windows des valeurs qui indiquent que le fournisseur DLL prend en charge les modèles de threads à thread unique (STA) et multithread apartment (MTA). Pour plus d’informations sur les modèles de thread COM, voir [Descriptions et fonctionnements des modèles de thread OLE.](https://support.microsoft.com/kb/150777)
    
Les méthodes dans l’extensibilité du fournisseur OSC doivent renvoyer des types primitifs tels que **chaîne** ou **bool**. Certaines **valeurs** de retour de chaîne doivent être conformes à la définition de schéma pour l’extensibilité du fournisseur OSC. Seul le XML est pris en charge comme valeur de retour. 
  
## <a name="details-of-the-osc-provider-extensibility-dll"></a>Détails de la DLL d’extensibilité du fournisseur OSC

Le composant qui prend en charge l’extensibilité du fournisseur OSC est la DLL d’extensibilité du fournisseur OSC. Les développeurs tiers peuvent créer des DLL de fournisseur OSC à l’aide de ces interfaces d’extensibilité. La liste suivante affiche les détails de la DLL d’extensibilité du fournisseur OSC :
  
- Nom de fichier DLL d’extensibilité : socialprovider.dll
    
- Nom convivial de la DLL d’extensibilité : Microsoft Outlook Social Provider Extensibility
    
- Extensibilité DLL version principale : 15.0
    
- Extensibiilty DLL TypeLib version: 1.1
    
## <a name="miscellaneous-technical-information"></a>Informations techniques diverses

JavaScript Object Notation (JSON) n’est pas pris en charge dans le modèle d’extensibilité du fournisseur OSC.
  
Il n’y a pas de dépendances sur un parseur XML. Le fournisseur OSC peut utiliser un analyseur XML inclus dans Office, tel que Microsoft XML Core Services® (MSXML), utiliser les fonctionnalités d’analyse XML intégrées à Microsoft .NET Framework ou utiliser un analyseur XML tiers. 
  
## <a name="see-also"></a>Voir aussi

- [Meilleures pratiques pour le développement d’un fournisseur](best-practices-for-developing-a-provider.md)  
- [Étapes rapides pour Learning développement d’un fournisseur](quick-steps-for-learning-to-develop-a-provider.md)
- [Déploiement d'un fournisseur](deploying-a-provider.md)  
- [Prise en main du développement d'un fournisseur Outlook Social Connector](getting-started-with-developing-an-outlook-social-connector-provider.md)

