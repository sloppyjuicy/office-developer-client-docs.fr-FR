---
title: HrProcessConvActionForSentItem
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: overview
localization_priority: Normal
ms.assetid: 08121e33-7820-4a31-b6da-06a4a54ec43f
description: Effectue la catégorisation post-envoi sur un élément de courrier en fonction de son PidTagConversationId.
ms.openlocfilehash: 675f308093eea30084271abc66c1fa66e2ad6828
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32318899"
---
# <a name="hrprocessconvactionforsentitem"></a>HrProcessConvActionForSentItem

Effectue la catégorisation post-envoi sur un élément de courrier en fonction de [son PidTagConversationId](https://msdn.microsoft.com/library/f8e4a5fa-cb73-4eca-b174-72e1fda821a6%28Office.15%29.aspx).
  
## <a name="quick-info"></a>Informations rapides

|||
|:-----|:-----|
|Exporté par :  <br/> |Outlook.exe  <br/> |
|Appelé par :  <br/> |Client  <br/> |
|Implémenté par :  <br/> |Outlook  <br/> |
   
```cpp
HRESULT WINAPI HrProcessConvActionForSentItem( 
    SBinary const *pmbinStoreEid, 
    SBinary const *pmbinMsgEid, 
    SBinary const *pmbinConvID, 
    DWORD dwFlags)
```

## <a name="parameters"></a>Parameters

_pmbinStoreEid_
  
> [in] [PidTagEntryId](https://msdn.microsoft.com/library/ca02e873-c2d2-4d58-8df8-c05fbcdc8fba%28Office.15%29.aspx) de la boutique ou [PidTagStoreEntryId](https://msdn.microsoft.com/library/0d705667-19f4-4eda-a068-e65ea8f00d9b%28Office.15%29.aspx) de l’élément de courrier. Ne peut pas être NULL ou non valide. 
    
_pmbinMsgEid_
  
> [in] [PidTagEntryId de](https://msdn.microsoft.com/library/ca02e873-c2d2-4d58-8df8-c05fbcdc8fba%28Office.15%29.aspx) l’élément de courrier. Ne peut pas être NULL ou non valide. 
    
_pmbinConvID_
  
> [in] [PidTagConversationId de](https://msdn.microsoft.com/library/f8e4a5fa-cb73-4eca-b174-72e1fda821a6%28Office.15%29.aspx) l’élément de courrier. Ne peut pas être NULL ou non valide. 
    
_dwFlags_
  
> [in] Masque de bits qui spécifie des informations supplémentaires sur l’appel de méthode.
    
   - 0 — Aucune option supplémentaire n’est utilisée dans cet appel de méthode. Il s’agit de la valeur recommandée. 
    
   - **PCAFSIF_MSGEID_IS_SEARCH_KEY**— _pmbinMsgEid_ est en fait [la clé PidTagSearchKey](https://msdn.microsoft.com/library/fcab369a-a1f4-4425-a272-e35046914a4d%28Office.15%29.aspx) du message. **L’utilisation d’une clé PidTagSearchKey** est intensive en ressources et doit être évitée si [un pidTagEntryId](https://msdn.microsoft.com/library/ca02e873-c2d2-4d58-8df8-c05fbcdc8fba%28Office.15%29.aspx) est disponible. 
    
## <a name="return-values"></a>Valeurs de retour

|**[HRESULT]**|**Description**|
|:-----|:-----|
|S_OK  <br/> |L’appel a réussi.  <br/> |
|E_INVALIDARG  <br/> | _dwFlags_ contient un indicateur inconnu.  <br/> |
   
## <a name="remarks"></a>Remarques

Les catégories sont considérées comme des informations personnelles et ne doivent pas être transmises en dehors de la boîte aux lettres de l’utilisateur. Par conséquent, n’appelez **pas HrProcessConvActionForSentItem** sur un élément de courrier non envoyé. Envoyez plutôt l’élément, puis appelez **HrProcessConvActionForSentItem** sur la copie archivée. La copie archivée peut être stockée dans le dossier Éléments envoyés ou dans un emplacement équivalent. 
  
Votre application doit être en cours de traitement avec Outlook.exe, par exemple à partir d’un compl?ment COM, pour appeler **HrProcessConvActionForSentItem**. Si vous essayez d’appeler **HrProcessConvActionForSentItem** hors processus, **HrProcessConvActionForSentItem** va lancer une exception de violation d’accès. 
  

