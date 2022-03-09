---
title: DNTBL
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
ms.assetid: 77835b48-43aa-8518-9712-754e84f1e713
description: 'Dernière modification : 05 juillet 2012'
ms.openlocfilehash: 743e7eb8ce3cc84ebb52c529f0b0fca778603395
ms.sourcegitcommit: 518845d053a009b11c8d907a33822161c0b6bc96
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/08/2022
ms.locfileid: "63375684"
---
# <a name="dntbl"></a>DNTBL
 
**S’applique à** : Outlook 2013 | Outlook 2016 
  
Informations relatives au téléchargement du contenu d’un dossier à partir du serveur pendant le [téléchargement de l’état de la table](download-table-state.md), dans le cadre d’une synchronisation complète du contenu dans une banque.
  
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

## <a name="members"></a>Membres

_ulFlags_
  
> [entrant] Indicateurs permettant de modifier le comportement

  - DNT_OK

    - [entrant] Téléchargement réussi. Le client définit cet élément après avoir téléchargé des informations à partir du serveur.

_pstmReserved1_
  
> [sortant] Ce membre est réservé à un usage interne d’Outlook et n’est pas pris en charge.

_pstmReserved2_
  
> [sortant] Ce membre est réservé à un usage interne d’Outlook et n’est pas pris en charge.

_pstmReserved3_
  
> [sortant] Ce membre est réservé à un usage interne d’Outlook et n’est pas pris en charge.

_pstmReserved4_
  
> [sortant] Ce membre est réservé à un usage interne d’Outlook et n’est pas pris en charge.

_pxicc_
  
> [sortant] Pointeur vers l’interface de contenu **IExchangeImportContentsChanges** prenant en charge le téléchargement des modifications de contenu. Pour plus d’informations sur **IExchangeImportContentsChanges**, reportez-vous à [Critères d’évaluation ICS](https://msdn.microsoft.com/library/aa579252%28EXCHG.80%29.aspx).

_pxihc_
  
> [sortant] Pointeur vers l’interface de hiérarchie **IExchangeImportHierarchyChanges** qui prend en charge le téléchargement des modifications de hiérarchie incrémentielle. Pour plus d’informations sur **IExchangeImportHierarchyChanges**, reportez-vous à [Critères d’évaluation ICS](https://msdn.microsoft.com/library/aa579252%28EXCHG.80%29.aspx).

_pszName_
  
> [sortant] Nom du dossier.

_ftLastMod_
  
> [sortant] Heure de la dernière modification du dossier.

_ulRights_
  
> [sortant] Valeur de la propriété **[PR_RIGHTS](https://msdn.microsoft.com/library/ee238052%28v=EXCHG.80%29.aspx)** du dossier.

_feid_
  
> [sortant] ID d’entrée du dossier.

_uintReserved_
  
> [sortant] Ce membre est réservé à un usage interne d’Outlook et n’est pas pris en charge.

_rgte_
  
> [sortant] Modifications pour les éléments normaux (ou non masqués) et les éléments associés (ou masqués). *rgte[0] est* pour les éléments normaux et *rgte[1]* pour les éléments associés. Outlook renseigne ce membre pendant le téléchargement lors de l’utilisation de la synchronisation des modifications incrémentielle (ICS). Pour plus d’informations sur ICS, reportez-vous à [Critères d’évaluation ICS](https://msdn.microsoft.com/library/aa579252%28EXCHG.80%29.aspx).

_lpsrReserved_
  
> [entrant]/[sortant] Ce membre est réservé à un usage interne d’Outlook et n’est pas pris en charge.

_boReserved_
  
> [entrant] Ce membre est réservé à un usage interne d’Outlook et n’est pas pris en charge.

_pReserved1_
  
> [sortant] Ce membre est réservé à un usage interne d’Outlook et n’est pas pris en charge.

_pReserved2_
  
> [entrant] Ce membre est réservé à un usage interne d’Outlook et n’est pas pris en charge.

## <a name="see-also"></a>Voir aussi

- [À propos de la machine à états de réplication](about-the-replication-state-machine.md)  
- [Constantes MAPI](mapi-constants.md)
- [DNTBLE](dntble.md)