---
title: MAPICrashRecovery
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
api_name:
- MAPICrashRecovery
api_type:
- COM
ms.assetid: 4172e2d3-6343-385b-c691-a64c1e198051
description: La fonction MAPICrashRecovery vérifie l’état de la mémoire partagée du fichier de dossiers personnels (PST) ou du fichier de dossiers en mode hors connexion (OST).
ms.openlocfilehash: 3865390c2183a3b25249dc63af880b052dc4e132
ms.sourcegitcommit: 0a067f44281eddabff15fff565fb80eaa543b660
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/23/2022
ms.locfileid: "63764502"
---
# <a name="mapicrashrecovery"></a>MAPICrashRecovery

**S’applique à** : Outlook 2013 | Outlook 2016 
  
La **fonction MAPICrashRecovery** vérifie l’état de la mémoire partagée du fichier de dossiers personnels (PST) ou du fichier de dossiers en mode hors connexion (OST). Si la mémoire est dans un état cohérent, la fonction **MAPICrashRecovery** déplace les données sur le disque et empêche tout accès en lecture ou en écriture jusqu’à ce que le processus soit terminé. 
  
## <a name="quick-info"></a>Informations rapides

|Propriété |Valeur |
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
    
   - **MAPICRASH\_ RECOVER** : si les PST ou osts sont dans un état cohérent, déplacez les données sur le disque et verrouillez les PST ou osts pour empêcher l’accès en lecture ou en écriture.
    
   - **MAPICRASH\_ CONTINUE**: Unlock the PSTs or OSTs for debugging. Après un appel réussi à **MAPICrashRecovery** avec l’indicateur **MAPICRASH_RECOVER**, appelez **MAPICrashRecovery** avec l’indicateur **MAPICRASHCONTINUE\_** pour autoriser le débogage. 
    
   - **MAPICRASH\_ SYSTEM_SHUTDOWN** : si les PST ou osts sont dans un état cohérent, déplacez les données sur le disque et verrouillez les PST ou osts pour empêcher l’accès en lecture ou en écriture. Les PST ou osts ne peuvent pas être déverrouillés à l’aide **de MAPICRASHCONTINUE\_**. Doit être utilisé en combinaison avec **MAPICRASHRECOVER\_**. 
    
## <a name="remarks"></a>Remarques

L’byte supérieur (0xFF000000) est réservé aux indicateurs de récupération d’incident spécifiques au fournisseur.
  
Appelez **MAPICrashRecovery** avec **les indicateurs MAPICRASHRECOVER\_** et **MAPICRASH_SYSTEM_SHUTDOWN** en réponse au message **WM_ENDSESSION** message. 
  
## <a name="see-also"></a>Voir aussi

- [À propos de l’API de récupération sur incident MAPI](about-the-mapi-crash-recovery-api.md)
- [Utiliser l’API de récupération sur incident MAPI](how-to-use-the-mapi-crash-recovery-api.md)

