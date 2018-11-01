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
ms.openlocfilehash: 66e23d73af53b05295bf2cbcd8c604ab3545bbca
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/23/2018
ms.locfileid: "22573137"
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

## <a name="parameters"></a>Param�tres

 _ulFlags_
  
> [in] Masque de bits d’indicateurs qui contrôle le type de la chaîne retournée. Vous pouvez définir l’indicateur suivant :
    
MAPI_UNICODE 
  
> La chaîne retournée est au format Unicode. Si l’indicateur MAPI_UNICODE n’est pas définie, la chaîne est au format ANSI.
    
 _pszDisplayName_
  
> [out] Pointeur vers une chaîne qui contient le nom complet du conteneur de formulaire.
    
## <a name="return-value"></a>Valeur renvoyée

S_OK 
  
> L'appel a r�ussi et a renvoy� la valeur attendue ou les valeurs.
    
## <a name="mfcmapi-reference"></a>Référence MFCMAPI

Pour voir un exemple de code MFCMAPI, consultez le tableau suivant.
  
|**Fichier**|**Fonction**|**Commentaire**|
|:-----|:-----|:-----|
|FormContainerDlg.cpp  <br/> |CFormContainerDlg::CFormContainerDlg  <br/> |MFCMAPI utilise la méthode **IMAPIFormContainer::GetDisplay** pour obtenir le nom du formulaire conteneur lors du rendu CFormContainerDlg.  <br/> |
   
## <a name="see-also"></a>Voir aussi



[IMAPIFormContainer : IUnknown](imapiformcontaineriunknown.md)


[MFCMAPI comme un exemple de Code](mfcmapi-as-a-code-sample.md)

