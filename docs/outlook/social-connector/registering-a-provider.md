---
title: Inscription d’un fournisseur
manager: soliver
ms.date: 03/05/2015
ms.audience: Developer
ms.topic: overview
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: b60b3634-4c8b-4273-97a0-0a8a5a8a5342
description: Cette rubrique décrit les emplacements du Registre Windows qui sont utilisés lorsque vous installez un fournisseur Outlook Social Connector (OSC).
ms.openlocfilehash: 3ec594ec94b045d2ceb583144781a5746b945b5c
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19787698"
---
# <a name="registering-a-provider"></a>Inscription d’un fournisseur

Cette rubrique décrit les emplacements du Registre Windows qui sont utilisés lorsque vous installez un fournisseur Outlook Social Connector (OSC).
  
## <a name="com-registration"></a>Enregistrement COM

Vous devez configurer le fournisseur OSC DLL à inscrire à l’aide de l’inscription automatique COM ou regsvr32 pendant l’installation. Enregistrement COM de la DLL du fournisseur enregistre le fournisseur OSC sous le `HKEY_CLASSES_ROOT` ruche du Registre. 
  
Un fournisseur OSC développé dans le code managé a un assembly de fournisseur COM visibles. Vous devez utiliser un domaine d’application distinct pour le composant fournisseur. Sinon, le fournisseur OSC utilise le domaine d’application partagée par défaut qui est utilisé par d’autres composants et le fournisseur peut ne pas fonctionne comme prévu.
  
## <a name="registering-provider-progid"></a>Inscription du fournisseur ProgID

Chaque fournisseur OSC doit enregistrer un identificateur programmatique (`ProgID`). Le programme d’installation fournisseur peut choisir un des emplacements suivants pour ajouter ou supprimer la `ProgID`:
  
- `HKEY_CURRENT_USER\Software\Microsoft\Office\Outlook\SocialConnector\SocialProviders`&ndash; Votre programme d’installation du fournisseur doit utiliser cet emplacement si le fournisseur est installé pour seulement l’utilisateur actuellement connecté.
    
- `HKEY_LOCAL_MACHINE\Software\Microsoft\Office\Outlook\SocialConnector\SocialProviders`&ndash; Votre programme d’installation du fournisseur doit utiliser cet emplacement si le fournisseur n’est installé pour tous les utilisateurs sur l’ordinateur.
    
L’OSC recherche pour le fournisseur `ProgID` dans les emplacements ci-dessus, à moins que l’ordinateur client Outlook 32 bits sur un système d’exploitation de Windows 64 bits. Dans ce cas, votre programme d’installation du fournisseur doit cliquer sur un des emplacements suivants dans le `HKEY_CURRENT_USER` ou `HKEY_LOCAL_MACHINE` ruche : 
  
- `HKEY_CURRENT_USER\Software\Wow6432Node\Microsoft\Office\Outlook\SocialConnector\SocialProviders`
    
- `HKEY_LOCAL_MACHINE\Software\Wow6432Node\Microsoft\Office\Outlook\SocialConnector\SocialProviders`
    
Pour une version Click-to-Run d’Office, le programme d’installation de votre fournisseur doit cliquer sur un des emplacements suivants dans la ruche HKEY_CURRENT_USER ou HKEY_LOCAL_MACHINE :
  
- `HKEY_CURRENT_USER\Software\Microsoft\Office\ClickToRun\REGISTRY\MACHINE\Software\Microsoft\Office\Outlook\SocialConnector\SocialProviders`
    
- `HKEY_LOCAL_MACHINE\Software\Microsoft\Office\ClickToRun\REGISTRY\MACHINE\Software\Microsoft\Outlook\SocialConnector\SocialProviders`
    
## <a name="see-also"></a>Voir aussi

- [Aide-mémoire d’installation](installation-checklist.md)
- [Étapes rapides pour apprendre à développer un fournisseur](quick-steps-for-learning-to-develop-a-provider.md)
- [Déploiement d'un fournisseur](deploying-a-provider.md)

