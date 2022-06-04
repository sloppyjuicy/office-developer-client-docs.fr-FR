---
title: UPMOV
description: Décrit les informations relatives au chargement d’éléments qui ont été déplacés. Ces informations sont utilisées pendant l’état de suppression de chargement et l’état de la table de chargement.
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
ms.assetid: 098743a5-f265-639a-8ba6-1412705bee0a
ms.openlocfilehash: 68b5c471f08b6965156f645565645267c76ea799
ms.sourcegitcommit: eb83b72d14a07ac316c71e8208397d1c7046f6df
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/04/2022
ms.locfileid: "65894088"
---
# <a name="upmov"></a>UPMOV
 
**S’applique à** : Outlook 2013 | Outlook 2016 
  
Informations sur le chargement d’éléments qui ont été déplacés. Ces informations sont utilisées pendant [l’état de suppression de chargement](upload-delete-status-state.md) et [l’état de la table de chargement](upload-table-state.md).
  
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
  
> [in] Indicateurs pour déterminer le comportement approprié pendant le chargement.
    
  - UPV_ERROR
    
    - [in] Problème lors de l’ouverture du dossier serveur.
    
  - UPV_DIRTY
    
    - [in] L’état de chargement a changé. Il est utilisé par le client pour suivre la modification de l’état du magasin local.
    
  - UPV_COMMIT
    
    - [in] Valider l’état de chargement.
    
_Conservés_
  
> [sortant] Ce membre est réservé à un usage interne d’Outlook et n’est pas pris en charge. 
    
_pstmReserved_
  
> [sortant] Ce membre est réservé à un usage interne d’Outlook et n’est pas pris en charge. 
    
_pszName_
  
> [out] Nom du dossier de destination. 
    
  > [!NOTE]
  > Ce membre ne prend pas en charge UNICODE. 
  
_feid_
  
> [out] ID d’entrée du dossier de destination. 
    
_pfld_
  
> [in] Pointeur vers le dossier serveur. 
    
_pxicc_
  
> [in] Pointeur vers l’interface de contenu **IExchangeImportContentsChanges** qui prend en charge le chargement des modifications de contenu lors de l’utilisation de la synchronisation incrémentielle des modifications (ICS). Pour plus d’informations sur **IExchangeImportContentsChanges** et ICS, consultez [critères d’évaluation ICS](https://msdn.microsoft.com/library/aa579252%28EXCHG.80%29.aspx).
    
_dwReserved_
  
> [sortant] Ce membre est réservé à un usage interne d’Outlook et n’est pas pris en charge. 
    
_pupmovNext_
  
> [out] Contexte de déplacement suivant. 
    
_cEntMov_
  
> [in] Nombre d’éléments déplacés ici. 
    
## <a name="see-also"></a>Voir aussi

- [À propos de l’API de réplication](about-the-replication-api.md)
- [À propos de la machine à états de réplication](about-the-replication-state-machine.md)
- [Constantes MAPI](mapi-constants.md)
- [FEID](feid.md)

