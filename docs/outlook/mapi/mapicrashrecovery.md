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
ms.openlocfilehash: 6b07d794a8f54477c6706cb70af60f7f7ef57d49
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/23/2018
ms.locfileid: "22595341"
---
# <a name="mapicrashrecovery"></a>MAPICrashRecovery

**S’applique à** : Outlook 2013 | Outlook 2016 
  
La fonction **MAPICrashRecovery** vérifie que l’état du fichier de dossiers personnels (PST) ou le fichier de dossiers en mode hors connexion (OST) de mémoire partagée. Si la mémoire est dans un état cohérent, la fonction **MAPICrashRecovery** déplace les données sur le disque et empêche plu accès en lecture ou écriture jusqu'à ce que le processus est terminé. 
  
## <a name="quick-info"></a>Informations rapides

|||
|:-----|:-----|
|Exportés par :  <br/> |olmapi32.dll  <br/> |
|Appelé par :  <br/> |Client  <br/> |
|Implémenté par :  <br/> |Outlook  <br/> |
   
```cpp
void MAPICrashRecovery(ULONG ulFlags);
```

## <a name="parameters"></a>Param�tres

_ulFlags_
  
> [in] Indicateurs utilisés pour contrôler la façon dont la récupération après incident MAPI est effectuée. Les indicateurs suivants peuvent être définis :
    
   - **MAPICRASH\_récupérer**: si les fichiers pst ou ost est dans un état cohérent, déplacer les données sur le disque et verrouiller les fichiers pst ou l’OST pour empêcher l’accès en lecture ou écriture.
    
   - **MAPICRASH\_continuer**: déverrouiller les fichiers pst ou ost pour le débogage. Après un appel réussi à **MAPICrashRecovery** avec l’indicateur **MAPICRASH_RECOVER** , appelez **MAPICrashRecovery** avec la **MAPICRASH\_continuer** indicateur pour autoriser le débogage continuer. 
    
   - **MAPICRASH\_SYSTEM_SHUTDOWN**: si les fichiers pst ou ost est dans un état cohérent, déplacer les données sur le disque et verrouiller les fichiers pst ou l’OST pour empêcher l’accès en lecture ou écriture. Les fichiers pst ou OST ne peut pas être déverrouillé à l’aide de **MAPICRASH\_continuer**. Doit être utilisée en combinaison avec **MAPICRASH\_récupérer**. 
    
## <a name="remarks"></a>Remarques

L’octet supérieur (0xFF000000) est réservé à des indicateurs de récupération fournisseur incident spécifique.
  
Appelez **MAPICrashRecovery** avec la **MAPICRASH\_récupérer** et indicateurs **MAPICRASH_SYSTEM_SHUTDOWN** en réponse au message **WM_ENDSESSION** . 
  
## <a name="see-also"></a>Voir aussi

- [À propos de l’API de récupération sur incident MAPI](about-the-mapi-crash-recovery-api.md)
- [Utiliser l’API de récupération sur incident MAPI](how-to-use-the-mapi-crash-recovery-api.md)

