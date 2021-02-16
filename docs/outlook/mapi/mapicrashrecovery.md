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
description: Dernière modification le 9 mars 2015
ms.openlocfilehash: 9efafbac55a2925e04b533e7c08388c026540dff
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33407213"
---
# <a name="mapicrashrecovery"></a>MAPICrashRecovery

**S’applique à** : Outlook 2013 | Outlook 2016 
  
La **fonction MAPICrashRecovery** vérifie l’état de la mémoire partagée du fichier de dossiers personnels (PST) ou du fichier de dossiers en mode hors connexion (OST). Si la mémoire est dans un état cohérent, la fonction **MAPICrashRecovery** déplace les données sur le disque et empêche tout accès en lecture ou en écriture jusqu’à ce que le processus soit terminé. 
  
## <a name="quick-info"></a>Informations rapides

|||
|:-----|:-----|
|Exporté par :  <br/> |olmapi32.dll  <br/> |
|Appelé par :  <br/> |Client  <br/> |
|Implémenté par :  <br/> |Outlook  <br/> |
   
```cpp
void MAPICrashRecovery(ULONG ulFlags);
```

## <a name="parameters"></a>Paramètres

_ulFlags_
  
> [in] Indicateurs utilisés pour contrôler la façon dont la récupération d’incident MAPI est effectuée. Les indicateurs suivants peuvent être définies :
    
   - **MAPICRASH \_ RECOVER**: si les PST ou osts sont dans un état cohérent, déplacez les données sur le disque et verrouillez les PST ou osts pour empêcher l’accès en lecture ou en écriture.
    
   - **MAPICRASH \_ CONTINUE**: Déverrouillez les PST ou osts pour le débogage. Après un appel réussi à **MAPICrashRecovery** avec l’indicateur **MAPICRASH_RECOVER,** appelez **MAPICrashRecovery** avec l’indicateur **MAPICRASH \_ CONTINUE** pour autoriser le débogage. 
    
   - **MAPICRASH \_ SYSTEM_SHUTDOWN**: si les PST ou osts sont dans un état cohérent, déplacez les données sur le disque et verrouillez les PST ou osts pour empêcher l’accès en lecture ou en écriture. Les PST ou osts ne peuvent pas être déverrouillés à l’aide **de MAPICRASH \_ CONTINUE**. Doit être utilisé en combinaison avec **MAPICRASH \_ RECOVER**. 
    
## <a name="remarks"></a>Remarques

L’byte supérieur (0xFF000000) est réservé aux indicateurs de récupération d’incident spécifiques au fournisseur.
  
Appelez **MAPICrashRecovery** avec les indicateurs **MAPICRASH \_ RECOVER** et **MAPICRASH_SYSTEM_SHUTDOWN** en réponse au message **WM_ENDSESSION** message. 
  
## <a name="see-also"></a>Voir aussi

- [À propos de l’API de récupération sur incident MAPI](about-the-mapi-crash-recovery-api.md)
- [Utiliser l’API de récupération sur incident MAPI](how-to-use-the-mapi-crash-recovery-api.md)

