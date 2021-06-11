---
title: IMAPIFormContainerGetDisplay
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IMAPIFormContainer.GetDisplay
api_type:
- COM
ms.assetid: 6829e273-4a75-4278-b58a-ae7543e075ac
description: Dernière modification le 9 mars 2015
ms.openlocfilehash: 994041d050df56fd3fa3c0e599542e05a202ad65
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33416131"
---
# <a name="imapiformcontainergetdisplay"></a>IMAPIFormContainer::GetDisplay

  
  
**S’applique à** : Outlook 2013 | Outlook 2016 
  
Renvoie le nom complet d’un conteneur de formulaire.
  
```cpp
HRESULT GetDisplay(
  ULONG ulFlags,
  LPSTR FAR * pszDisplayName
);
```

## <a name="parameters"></a>Parameters

 _ulFlags_
  
> [in] Masque de bits d’indicateurs qui contrôle le type de la chaîne renvoyée. L’indicateur suivant peut être définie :
    
MAPI_UNICODE 
  
> La chaîne renvoyée est au format Unicode. Si l MAPI_UNICODE n’est pas définie, la chaîne est au format ANSI.
    
 _pszDisplayName_
  
> [out] Pointeur vers une chaîne qui contient le nom complet du conteneur de formulaires.
    
## <a name="return-value"></a>Valeur renvoyée

S_OK 
  
> L'appel a r�ussi et a renvoy� la valeur attendue ou les valeurs.
    
## <a name="mfcmapi-reference"></a>Référence MFCMAPI

Pour voir un exemple de code MFCMAPI, consultez le tableau suivant.
  
|**Fichier**|**Fonction**|**Commentaire**|
|:-----|:-----|:-----|
|FormContainerDlg.cpp  <br/> |CFormContainerDlg::CFormContainerDlg  <br/> |MFCMAPI utilise la méthode **IMAPIFormContainer::GetDisplay** pour obtenir le nom du conteneur de formulaires lors du rendu de CFormContainerDlg.  <br/> |
   
## <a name="see-also"></a>Voir aussi



[IMAPIFormContainer : IUnknown](imapiformcontaineriunknown.md)


[MFCMAPI comme un exemple de Code](mfcmapi-as-a-code-sample.md)

