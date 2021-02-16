---
title: Inscription d’un fournisseur
manager: soliver
ms.date: 03/05/2015
ms.audience: Developer
ms.topic: overview
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: b60b3634-4c8b-4273-97a0-0a8a5a8a5342
description: Cette rubrique décrit les emplacements du Registre Windows utilisés lorsque vous installez un fournisseur Outlook Social Connector (OSC).
ms.openlocfilehash: a5f76850f9bebcba3c2bff31e799a3b012d6b91a
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33421759"
---
# <a name="registering-a-provider"></a>Inscription d’un fournisseur

Cette rubrique décrit les emplacements du Registre Windows utilisés lorsque vous installez un fournisseur Outlook Social Connector (OSC).
  
## <a name="com-registration"></a>Inscription COM

Vous devez configurer la DLL du fournisseur OSC pour qu’elle s’inscrive à l’aide de l’auto-inscription COM ou de regsvr32 pendant l’installation. L’inscription COM de la DLL du fournisseur inscrit le fournisseur OSC sous la `HKEY_CLASSES_ROOT` ruche du Registre. 
  
Un fournisseur OSC développé en code géré possède un assembly de fournisseur visible par COM. Vous devez utiliser un domaine d’application distinct pour le composant fournisseur. Dans le cas contraire, le fournisseur OSC utilise le domaine d’application partagé par défaut qui est utilisé par d’autres composants et le fournisseur risque de ne pas fonctionner comme prévu.
  
## <a name="registering-provider-progid"></a>Inscription du fournisseur ProgID

Chaque fournisseur OSC doit inscrire un identificateur programmatique ( `ProgID` ). Le programme d’installation du fournisseur peut choisir l’un des emplacements suivants pour ajouter ou supprimer le `ProgID` :
  
- `HKEY_CURRENT_USER\Software\Microsoft\Office\Outlook\SocialConnector\SocialProviders`Votre programme d’installation de fournisseur doit utiliser cet emplacement si le fournisseur est installé uniquement pour l’utilisateur &ndash; actuellement connecté.
    
- `HKEY_LOCAL_MACHINE\Software\Microsoft\Office\Outlook\SocialConnector\SocialProviders`Votre programme d’installation de fournisseur doit utiliser cet emplacement si le fournisseur est installé pour tous les &ndash; utilisateurs sur l’ordinateur.
    
L’OSC recherche le fournisseur aux emplacements ci-dessus, sauf si Outlook 32 bits s’exécute sur un système d’exploitation  `ProgID` Windows 64 bits. Dans ce cas, votre programme d’installation de fournisseur doit choisir l’un des emplacements suivants dans  `HKEY_CURRENT_USER` la  `HKEY_LOCAL_MACHINE` ruche : 
  
- `HKEY_CURRENT_USER\Software\Wow6432Node\Microsoft\Office\Outlook\SocialConnector\SocialProviders`
    
- `HKEY_LOCAL_MACHINE\Software\Wow6432Node\Microsoft\Office\Outlook\SocialConnector\SocialProviders`
    
Pour une version « Exécuter en un clic d’Office , votre programme d’installation de fournisseur doit choisir l’un des emplacements suivants dans la HKEY_CURRENT_USER ou HKEY_LOCAL_MACHINE suivante :
  
- `HKEY_CURRENT_USER\Software\Microsoft\Office\ClickToRun\REGISTRY\MACHINE\Software\Microsoft\Office\Outlook\SocialConnector\SocialProviders`
    
- `HKEY_LOCAL_MACHINE\Software\Microsoft\Office\ClickToRun\REGISTRY\MACHINE\Software\Microsoft\Outlook\SocialConnector\SocialProviders`
    
## <a name="see-also"></a>Voir aussi

- [Liste de vérification de l’installation](installation-checklist.md)
- [Étapes rapides pour apprendre à développer un fournisseur](quick-steps-for-learning-to-develop-a-provider.md)
- [Déploiement d'un fournisseur](deploying-a-provider.md)

