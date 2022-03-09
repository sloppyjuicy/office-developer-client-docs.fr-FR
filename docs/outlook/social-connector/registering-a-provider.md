---
title: Inscription d’un fournisseur
manager: soliver
ms.date: 03/05/2015
ms.audience: Developer
ms.topic: overview
ms.prod: office-online-server
ms.localizationpriority: medium
ms.assetid: b60b3634-4c8b-4273-97a0-0a8a5a8a5342
description: Cette rubrique décrit les emplacements Windows registre utilisés lors de l’installation d’un fournisseur OSC (Outlook Social Connector).
ms.openlocfilehash: 473a1a3c1c8bb2d2d9419ecc20a92b0341f4f01f
ms.sourcegitcommit: 518845d053a009b11c8d907a33822161c0b6bc96
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/08/2022
ms.locfileid: "63379877"
---
# <a name="registering-a-provider"></a>Inscription d’un fournisseur

Cette rubrique décrit les emplacements Windows registre utilisés lors de l’installation d’un fournisseur OSC (Outlook Social Connector).
  
## <a name="com-registration"></a>Inscription COM

Vous devez configurer la DLL du fournisseur OSC pour qu’elle s’inscrive à l’aide de l’auto-inscription COM ou de regsvr32 pendant l’installation. L’inscription COM de la DLL du fournisseur inscrit le fournisseur OSC sous la `HKEY_CLASSES_ROOT` ruche du Registre.
  
Un fournisseur OSC développé en code géré possède un assembly de fournisseur visible par COM. Vous devez utiliser un domaine d’application distinct pour le composant fournisseur. Dans le cas contraire, le fournisseur OSC utilise le domaine d’application partagé par défaut qui est utilisé par d’autres composants et le fournisseur risque de ne pas fonctionner comme prévu.
  
## <a name="registering-provider-progid"></a>Inscription du fournisseur ProgID

Chaque fournisseur OSC doit inscrire un identificateur programmatique (`ProgID`). Le programme d’installation du fournisseur peut choisir l’un des emplacements suivants pour ajouter ou supprimer le :`ProgID`
  
- `HKEY_CURRENT_USER\Software\Microsoft\Office\Outlook\SocialConnector\SocialProviders`&ndash; Votre programme d’installation de fournisseur doit utiliser cet emplacement si le fournisseur est installé uniquement pour l’utilisateur actuellement connecté.

- `HKEY_LOCAL_MACHINE\Software\Microsoft\Office\Outlook\SocialConnector\SocialProviders`&ndash; Votre programme d’installation de fournisseur doit utiliser cet emplacement si le fournisseur est installé pour tous les utilisateurs sur l’ordinateur.

L’OSC `ProgID` recherche le fournisseur aux emplacements ci-dessus, sauf si l’ordinateur client dispose de Outlook 32 bits en cours d’exécution sur un système d’exploitation Windows 64 bits. Dans ce cas, votre programme d’installation de fournisseur doit choisir l’un des emplacements suivants dans la `HKEY_CURRENT_USER` ruche `HKEY_LOCAL_MACHINE` :
  
- `HKEY_CURRENT_USER\Software\Wow6432Node\Microsoft\Office\Outlook\SocialConnector\SocialProviders`

- `HKEY_LOCAL_MACHINE\Software\Wow6432Node\Microsoft\Office\Outlook\SocialConnector\SocialProviders`

Pour une version « Click-to-Run de Office , votre programme d’installation de fournisseur doit choisir l’un des emplacements suivants dans la ruche HKEY_CURRENT_USER ou HKEY_LOCAL_MACHINE suivante :
  
- `HKEY_CURRENT_USER\Software\Microsoft\Office\ClickToRun\REGISTRY\MACHINE\Software\Microsoft\Office\Outlook\SocialConnector\SocialProviders`

- `HKEY_LOCAL_MACHINE\Software\Microsoft\Office\ClickToRun\REGISTRY\MACHINE\Software\Microsoft\Outlook\SocialConnector\SocialProviders`

## <a name="see-also"></a>Voir aussi

- [Liste de vérification de l’installation](installation-checklist.md)
- [Étapes rapides pour Learning développement d’un fournisseur](quick-steps-for-learning-to-develop-a-provider.md)
- [Déploiement d'un fournisseur](deploying-a-provider.md)
