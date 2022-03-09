---
title: DNHIER
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
ms.assetid: 3953dc9d-0146-3689-63f0-c6ba78566b8b
description: 'Dernière modification : 05 juillet 2012'
ms.openlocfilehash: 7e9ded850ee8555a14697cf07a173d57e7ec5115
ms.sourcegitcommit: 518845d053a009b11c8d907a33822161c0b6bc96
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/08/2022
ms.locfileid: "63376650"
---
# <a name="dnhier"></a>DNHIER

**S’applique à** : Outlook 2013 | Outlook 2016
  
Informations relatives au téléchargement d’une hiérarchie à partir du serveur pendant le [téléchargement de l’état de la hiérarchie](download-hierarchy-state.md), qui fait partie d’une synchronisation de la hiérarchie complète. Ce processus de téléchargement utilise une méthode de synchronisation des modifications incrémentielle (ICS) de Microsoft Exchange. Pour plus d’informations sur ICS, reportez-vous à [Critères d’évaluation ICS](https://msdn.microsoft.com/library/aa579252%28EXCHG.80%29.aspx).
  
## <a name="quick-info"></a>Informations rapides

```cpp
struct DNHIER 
{ 
    ULONG ulFlags; 
    LPSTREAM pstmReserved; 
    PXIHC pxihc; 
    UINT cEntNew; 
   UINT cEntMod; 
    UINT cEntDel; 
};
```

## <a name="members"></a>Membres

_ulFlags_
  
> [entrant] Indicateurs permettant de déterminer le comportement approprié pendant le téléchargement.

- DNH_OK

- [entrant] Téléchargement réussi. Le client définit cet élément après avoir téléchargé des informations à partir du serveur.

_pstmReserved_
  
> [sortant] Ce membre est réservé à un usage interne d’Outlook et n’est pas pris en charge.

_pxihc_
  
> [sortant] Pointeur vers l’interface de hiérarchie **IExchangeImportHierarchyChanges** qui prend en charge le téléchargement des modifications de hiérarchie incrémentielle. Pour plus d’informations sur **IExchangeImportHierarchyChanges**, reportez-vous à [Critères d’évaluation ICS](https://msdn.microsoft.com/library/aa579252%28EXCHG.80%29.aspx).

_cEntNew_
  
> [sortant] Nombre de dossiers ajoutés à la banque locale. Outlook renseigne cette valeur pendant le téléchargement lors de l’utilisation d’ICS.

_cEntMod_
  
> [sortant] Nombre de dossiers à modifier dans la banque locale. Outlook renseigne cette valeur pendant le téléchargement lors de l’utilisation d’ICS.

_cEntDel_
  
> [sortant] Nombre de dossiers à supprimer de la banque locale. Outlook renseigne cette valeur pendant le téléchargement lors de l’utilisation d’ICS.

## <a name="see-also"></a>Voir aussi

- [À propos de la machine à états de réplication](about-the-replication-state-machine.md)
- [Constantes MAPI](mapi-constants.md)
