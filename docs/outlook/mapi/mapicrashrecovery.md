---
title: MAPICrashRecovery
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPICrashRecovery
api_type:
- COM
ms.assetid: 4172e2d3-6343-385b-c691-a64c1e198051
description: 'Derni�re modification�: lundi 9 mars 2015'
ms.openlocfilehash: 9efafbac55a2925e04b533e7c08388c026540dff
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32357301"
---
# <a name="mapicrashrecovery"></a>MAPICrashRecovery

**S’applique à** : Outlook 2013 | Outlook 2016 
  
La fonction **MAPICrashRecovery** vérifie l'état du fichier de dossiers personnels (PST) ou de la mémoire partagée du fichier de dossiers en mode hors connexion (OST). Si la mémoire est dans un état cohérent, la fonction **MAPICrashRecovery** déplace les données sur le disque et empêche l'accès en lecture ou en écriture tant que le processus n'est pas terminé. 
  
## <a name="quick-info"></a>Informations rapides

|||
|:-----|:-----|
|Exporté par:  <br/> |olmapi32. dll  <br/> |
|Appelé par :  <br/> |Client  <br/> |
|Implémenté par :  <br/> |Outlook  <br/> |
   
```cpp
void MAPICrashRecovery(ULONG ulFlags);
```

## <a name="parameters"></a>Paramètres

_ulFlags_
  
> dans Indicateurs utilisés pour contrôler la manière dont la récupération d'urgence MAPI est effectuée. Les indicateurs suivants peuvent être définis:
    
   - **MAPICRASH\_Recover**: si les fichiers PST ou OSTs sont dans un état cohérent, déplacez les données sur le disque et verrouillez les fichiers PST ou OSTs pour empêcher l'accès en lecture ou en écriture.
    
   - **MAPICRASH\_continue**: Déverrouillez les fichiers PST ou OSTs pour le débogage. Après un appel réussi à **MAPICrashRecovery** avec l'indicateur **MAPICRASH_RECOVER** , appelez **MAPICrashRecovery** avec l' **indicateur\_MAPICRASH continue** pour autoriser le débogage. 
    
   - **MAPICRASH\_SYSTEM_SHUTDOWN**: si les fichiers PST ou OSTs sont dans un état cohérent, déplacez les données sur le disque et verrouillez les fichiers PST ou OSTs pour empêcher l'accès en lecture ou en écriture. Les fichiers PST ou OSTs ne peuvent pas être déverrouillés à l'aide de **MAPICRASH\_continuer**. Doit être utilisé en combinaison avec **MAPICRASH\_Recover**. 
    
## <a name="remarks"></a>Remarques

L'octet supérieur (0xFF000000) est réservé aux indicateurs de récupération d'incidents spécifiques au fournisseur.
  
Appelez **MAPICrashRecovery** avec les **indicateurs\_MAPICRASH Recover** et **MAPICRASH_SYSTEM_SHUTDOWN** en réponse au message **WM_ENDSESSION** . 
  
## <a name="see-also"></a>Voir aussi

- [À propos de l’API de récupération sur incident MAPI](about-the-mapi-crash-recovery-api.md)
- [Utiliser l’API de récupération sur incident MAPI](how-to-use-the-mapi-crash-recovery-api.md)

