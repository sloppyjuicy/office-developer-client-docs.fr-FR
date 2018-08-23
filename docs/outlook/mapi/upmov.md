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
ms.openlocfilehash: 0a8e318f9bb5e538473e1b60c650e8730f692e50
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/23/2018
ms.locfileid: "22577988"
---
# <a name="upmov"></a>UPMOV
 
**S’applique à**: Outlook 2013 | Outlook 2016 
  
Informations de téléchargement des éléments qui ont été déplacés. Ces informations sont utilisées lors du [téléchargement supprimer l’état](upload-delete-status-state.md) et [Télécharger l’état de la table](upload-table-state.md).
  
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

## <a name="members"></a>Members

_ulFlags_
  
> [in] Indicateurs pour déterminer le comportement approprié lors du téléchargement.
    
  - UPV_ERROR
    
    - [in] Problème d’ouverture de dossier du serveur.
    
  - UPV_DIRTY
    
    - [in] L’état du téléchargement a changé. Il est utilisé par le client pour effectuer le suivi de la modification de l’état pour le magasin local.
    
  - UPV_COMMIT
    
    - [in] Valider l’état du téléchargement.
    
_Conservés_
  
>  [out] Ce membre est réservé à un usage interne d’Outlook et n’est pas pris en charge. 
    
_pstmReserved_
  
>  [out] Ce membre est réservé à un usage interne d’Outlook et n’est pas pris en charge. 
    
_pszName_
  
>  [out] Nom du dossier de destination. 
    
  > [!NOTE]
  > Ce membre ne prend pas en charge UNICODE. 
  
_feid_
  
>  [out] ID d’entrée du dossier de destination. 
    
_pfld_
  
>  [in] Pointeur vers le dossier du serveur. 
    
_pxicc_
  
>  [in] Pointeur vers l’interface de contenu **IExchangeImportContentsChanges** qui prend en charge le téléchargement des modifications du contenu lors de l’utilisation de la synchronisation de modification incrémentielle (ICS). Pour plus d’informations sur **IExchangeImportContentsChanges** et partage de connexion Internet, voir [Critères d’évaluation de partage de connexion Internet](http://msdn.microsoft.com/en-us/library/aa579252%28EXCHG.80%29.aspx).
    
_dwReserved_
  
>  [out] Ce membre est réservé à un usage interne d’Outlook et n’est pas pris en charge. 
    
_pupmovNext_
  
>  [out] Déplacez ensuite le contexte. 
    
_cEntMov_
  
>  [in] Nombre d’éléments déplacés ici. 
    
## <a name="see-also"></a>Voir aussi

- [À propos de l’API de réplication](about-the-replication-api.md)
- [À propos de la machine à états de réplication](about-the-replication-state-machine.md)
- [Constantes MAPI](mapi-constants.md)
- [FEID](feid.md)

