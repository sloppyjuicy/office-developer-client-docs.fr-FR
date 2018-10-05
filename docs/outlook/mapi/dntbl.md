---
title: DNTBL
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 77835b48-43aa-8518-9712-754e84f1e713
description: 'Derni�re modification�: jeudi 5 juillet 2012'
ms.openlocfilehash: 4716a6f42968d7451a5db36173c4e6a9e843c08e
ms.sourcegitcommit: ef717c65d8dd41ababffb01eafc443c79950aed4
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 10/04/2018
ms.locfileid: "25398121"
---
# <a name="dntbl"></a>DNTBL
 
**S’applique à** : Outlook 2013 | Outlook 2016 
  
Informations pour le téléchargement du contenu d’un dossier à partir du serveur au cours de l' [état de la table du téléchargement](download-table-state.md), dans le cadre d’une synchronisation complète pour le contenu sur un magasin.
  
## <a name="quick-info"></a>Informations rapides

```cpp
struct DNTBL 
{ 
    ULONG ulFlags; 
    LPSTREAM pstmReserved1; 
    LPSTREAM pstmReserved2; 
    LPSTREAM pstmReserved3; 
    LPSTREAM pstmReserved4; 
    PXICC pxicc; 
    PXIHC pxihc; 
    LPSTR pszName; 
    FILETIME ftLastMod; 
    ULONG ulRights; 
    FEID feid; 
    UINT uintReserved; 
    DNTBLE rgte[2]; 
    LPSRestriction psrReserved; 
    BOOL boReserved; 
    void* pReserved1; 
    void* pReserved2; 
};

```

## <a name="members"></a>Members

_ulFlags_
  
> [in] Indicateurs pour modifier le comportement 
    
  - DNT_OK
    
    - [in] Téléchargement a réussi. Le client définit après le téléchargement des informations à partir du serveur.
    
_pstmReserved1_
  
> [out] Ce membre est réservé à un usage interne d’Outlook et n’est pas pris en charge. 
    
_pstmReserved2_
  
> [out] Ce membre est réservé à un usage interne d’Outlook et n’est pas pris en charge. 
    
_pstmReserved3_
  
> [out] Ce membre est réservé à un usage interne d’Outlook et n’est pas pris en charge. 
    
_pstmReserved4_
  
> [out] Ce membre est réservé à un usage interne d’Outlook et n’est pas pris en charge. 
    
_pxicc_
  
>  [out] Pointeur vers l’interface de contenu **IExchangeImportContentsChanges** qui prend en charge le téléchargement des modifications de contenu. Pour plus d’informations sur **IExchangeImportContentsChanges**, voir [Critères d’évaluation de partage de connexion Internet](https://msdn.microsoft.com/library/aa579252%28EXCHG.80%29.aspx).
    
_pxihc_
  
>  [out] Pointeur vers l’interface de hiérarchie **IExchangeImportHierarchyChanges** qui prend en charge le téléchargement des modifications incrémentielles de hiérarchie. Pour plus d’informations sur **IExchangeImportHierarchyChanges**, voir [Critères d’évaluation de partage de connexion Internet](https://msdn.microsoft.com/library/aa579252%28EXCHG.80%29.aspx).
    
_pszName_
  
>  [out] Nom du dossier. 
    
_ftLastMod_
  
>  [out] Heure de dernière modification du dossier. 
    
_ulRights_
  
>  [out] Valeur de la propriété **[PR_RIGHTS](https://msdn.microsoft.com/library/ee238052%28v=EXCHG.80%29.aspx)** du dossier. 
    
_feid_
  
>  [out] ID d’entrée du dossier. 
    
_uintReserved_
  
>  [out] Ce membre est réservé à un usage interne d’Outlook et n’est pas pris en charge. 
    
_rgte_
  
> [out] Modifications normal (ou non masqués) et les éléments associés (ou masqués).  *rgte [0]* est pour les éléments normales et *rgte [1]* est des éléments associés. Outlook remplit ce membre pendant le téléchargement lors de l’utilisation de la synchronisation de modification incrémentielle (ICS). Pour plus d’informations sur le partage de connexion Internet, voir [Critères d’évaluation de partage de connexion Internet](https://msdn.microsoft.com/library/aa579252%28EXCHG.80%29.aspx).
    
_lpsrReserved_
  
>  [in] / [out] ce membre est réservé à un usage interne d’Outlook et n’est pas pris en charge. 
    
_boReserved_
  
>  [in] Ce membre est réservé à un usage interne d’Outlook et n’est pas pris en charge. 
    
_pReserved1_
  
>  [out] Ce membre est réservé à un usage interne d’Outlook et n’est pas pris en charge. 
    
_pReserved2_
  
>  [in] Ce membre est réservé à un usage interne d’Outlook et n’est pas pris en charge. 
    
## <a name="see-also"></a>Voir aussi

- [À propos de la machine à états de réplication](about-the-replication-state-machine.md)  
- [Constantes MAPI](mapi-constants.md) 
- [DNTBLE](dntble.md)

