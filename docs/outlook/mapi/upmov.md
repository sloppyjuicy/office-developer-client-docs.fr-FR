---
title: UPMOV
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 098743a5-f265-639a-8ba6-1412705bee0a
description: 'Derni�re modification�: jeudi 5 juillet 2012'
ms.openlocfilehash: a7588d5fed2e059be7e628d8a76a12f76aea734d
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32339185"
---
# <a name="upmov"></a>UPMOV
 
**S’applique à** : Outlook 2013 | Outlook 2016 
  
Informations de téléchargement des éléments qui ont été déplacés. Ces informations sont utilisées lors de l'état de la [suppression du chargement](upload-delete-status-state.md) et de l'état de la [table de chargement](upload-table-state.md).
  
## <a name="quick-info"></a>Informations rapides

```cpp
struct UPMOV 
{ 
      ULONG          ulFlags; 
      LPVOID         pReserved; 
      LPSTREAM       pstmReserved; 
      LPSTR          pszName; 
      FEID           feid; 
      LPMAPIFOLDER   pfld; 
      PXICC          pxicc; 
      DWORD          dwReserved; 
      PUPMOV         pupmovNext; 
      UINT           cEntMov; 
};
```

## <a name="members"></a>Membres

_ulFlags_
  
> dans Indicateurs permettant de déterminer le comportement approprié pendant le chargement.
    
  - UPV_ERROR
    
    - dans Problème lors de l'ouverture du dossier du serveur.
    
  - UPV_DIRTY
    
    - dans L'état du chargement a changé. Cette option est utilisée par le client pour effectuer le suivi de la modification de l'État pour le magasin local.
    
  - UPV_COMMIT
    
    - dans Valider l'état du chargement.
    
_Disparition_
  
>  [sortant] Ce membre est réservé à un usage interne d’Outlook et n’est pas pris en charge. 
    
_pstmReserved_
  
>  [sortant] Ce membre est réservé à un usage interne d’Outlook et n’est pas pris en charge. 
    
_pszName_
  
>  remarquer Nom du dossier de destination. 
    
  > [!NOTE]
  > Ce membre ne prend pas en charge UNICODE. 
  
_feid_
  
>  remarquer ID d'entrée du dossier de destination. 
    
_pfld_
  
>  dans Pointeur vers le dossier du serveur. 
    
_pxicc_
  
>  dans Pointeur vers l'interface de contenu **IExchangeImportContentsChanges** qui prend en charge le téléchargement de modifications de contenu lors de l'utilisation de la synchronisation des modifications incrémentielles (ICS). Pour plus d'informations sur **IExchangeImportContentsChanges** et ICS, consultez la rubrique [critères d'évaluation ICS](https://msdn.microsoft.com/library/aa579252%28EXCHG.80%29.aspx).
    
_dwReserved_
  
>  [sortant] Ce membre est réservé à un usage interne d’Outlook et n’est pas pris en charge. 
    
_pupmovNext_
  
>  remarquer Contexte de déplacement suivant. 
    
_cEntMov_
  
>  dans Nombre d'éléments déplacés ici. 
    
## <a name="see-also"></a>Voir aussi

- [À propos de l’API de réplication](about-the-replication-api.md)
- [À propos de la machine à états de réplication](about-the-replication-state-machine.md)
- [Constantes MAPI](mapi-constants.md)
- [FEID](feid.md)

