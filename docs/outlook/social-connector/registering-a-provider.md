---
title: Inscription d’un fournisseur
manager: soliver
ms.date: 03/05/2015
ms.audience: Developer
ms.topic: overview
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: b60b3634-4c8b-4273-97a0-0a8a5a8a5342
description: Cette rubrique décrit les emplacements de Registre Windows qui sont utilisés lors de l'installation d'un fournisseur Outlook Social Connector (OSC).
ms.openlocfilehash: a5f76850f9bebcba3c2bff31e799a3b012d6b91a
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33421759"
---
# <a name="registering-a-provider"></a>Inscription d’un fournisseur

Cette rubrique décrit les emplacements de Registre Windows qui sont utilisés lors de l'installation d'un fournisseur Outlook Social Connector (OSC).
  
## <a name="com-registration"></a>Inscription COM

Vous devez configurer la DLL du fournisseur OSC pour enregistrer à l'aide de l'auto-enregistrement COM ou de regsvr32 lors de l'installation. L'inscription COM de la DLL du fournisseur enregistre le fournisseur OSC sous `HKEY_CLASSES_ROOT` la ruche de registre. 
  
Un fournisseur OSC développé dans le code managé dispose d'un assembly de fournisseur visible par COM. Vous devez utiliser un domaine d'application distinct pour le composant fournisseur. Dans le cas contraire, le fournisseur OSC utilise le domaine d'application partagé par défaut qui est utilisé par d'autres composants, et le fournisseur peut ne pas fonctionner comme prévu.
  
## <a name="registering-provider-progid"></a>Inscription du ProgID du fournisseur

Chaque fournisseur OSC doit inscrire un identificateur programmatique (`ProgID`). Le programme d'installation du fournisseur peut choisir l'un des emplacements suivants pour ajouter `ProgID`ou supprimer:
  
- `HKEY_CURRENT_USER\Software\Microsoft\Office\Outlook\SocialConnector\SocialProviders`&ndash; Le programme d'installation de votre fournisseur doit utiliser cet emplacement si le fournisseur est installé uniquement pour l'utilisateur actuellement connecté.
    
- `HKEY_LOCAL_MACHINE\Software\Microsoft\Office\Outlook\SocialConnector\SocialProviders`&ndash; Le programme d'installation de votre fournisseur doit utiliser cet emplacement si le fournisseur est installé pour tous les utilisateurs sur l'ordinateur.
    
Le OSC recherche le fournisseur `ProgID` aux emplacements ci-dessus, sauf si l'ordinateur client dispose d'Outlook 32 bits s'exécutant sur un système d'exploitation Windows 64 bits. Dans ce cas, le programme d'installation de votre fournisseur doit choisir l'un des emplacements `HKEY_CURRENT_USER` suivants `HKEY_LOCAL_MACHINE` dans la ruche ou: 
  
- `HKEY_CURRENT_USER\Software\Wow6432Node\Microsoft\Office\Outlook\SocialConnector\SocialProviders`
    
- `HKEY_LOCAL_MACHINE\Software\Wow6432Node\Microsoft\Office\Outlook\SocialConnector\SocialProviders`
    
Pour une version «démarrer en un clic» d'Office, le programme d'installation de votre fournisseur doit choisir l'un des emplacements suivants dans la ruche HKEY_CURRENT_USER ou HKEY_LOCAL_MACHINE:
  
- `HKEY_CURRENT_USER\Software\Microsoft\Office\ClickToRun\REGISTRY\MACHINE\Software\Microsoft\Office\Outlook\SocialConnector\SocialProviders`
    
- `HKEY_LOCAL_MACHINE\Software\Microsoft\Office\ClickToRun\REGISTRY\MACHINE\Software\Microsoft\Outlook\SocialConnector\SocialProviders`
    
## <a name="see-also"></a>Voir aussi

- [Liste de vérification de l'installation](installation-checklist.md)
- [Étapes rapides pour apprendre à développer un fournisseur](quick-steps-for-learning-to-develop-a-provider.md)
- [Déploiement d'un fournisseur](deploying-a-provider.md)

