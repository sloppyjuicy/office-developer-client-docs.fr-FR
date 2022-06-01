---
title: IMAPIFormContainerGetDisplay
description: IMAPIFormContainerGetDisplay retourne le nom complet d’un conteneur de formulaires. Cet article décrit sa syntaxe, ses paramètres et sa valeur de retour.
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
api_name:
- IMAPIFormContainer.GetDisplay
api_type:
- COM
ms.assetid: 6829e273-4a75-4278-b58a-ae7543e075ac
ms.openlocfilehash: 03e27237c0b058df755f41ca89769451310e7766
ms.sourcegitcommit: f872848fbeb5b2353179ad4bf4eab23f61f87666
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/01/2022
ms.locfileid: "65817731"
---
# <a name="imapiformcontainergetdisplay"></a>IMAPIFormContainer::GetDisplay

  
  
**S’applique à** : Outlook 2013 | Outlook 2016 
  
Retourne le nom complet d’un conteneur de formulaires.
  
```cpp
HRESULT GetDisplay(
  ULONG ulFlags,
  LPSTR FAR * pszDisplayName
);
```

## <a name="parameters"></a>Paramètres

 _ulFlags_
  
> [in] Masque de bits des indicateurs qui contrôle le type de la chaîne retournée. L’indicateur suivant peut être défini :
    
MAPI_UNICODE 
  
> La chaîne retournée est au format Unicode. Si l’indicateur MAPI_UNICODE n’est pas défini, la chaîne est au format ANSI.
    
 _pszDisplayName_
  
> [out] Pointeur vers une chaîne qui contient le nom complet du conteneur de formulaires.
    
## <a name="return-value"></a>Valeur renvoyée

S_OK 
  
> L'appel a r�ussi et a renvoy� la valeur attendue ou les valeurs.
    
## <a name="mfcmapi-reference"></a>Référence MFCMAPI

Pour voir un exemple de code MFCMAPI, consultez le tableau suivant.
  
|**Fichier**|**Fonction**|**Commentaire**|
|:-----|:-----|:-----|
|FormContainerDlg.cpp  <br/> |CFormContainerDlg::CFormContainerDlg  <br/> |MFCMAPI utilise la méthode **IMAPIFormContainer::GetDisplay** pour obtenir le nom du conteneur de formulaires lorsqu’il affiche CFormContainerDlg. |
   
## <a name="see-also"></a>Voir aussi



[IMAPIFormContainer : IUnknown](imapiformcontaineriunknown.md)


[MFCMAPI comme un exemple de Code](mfcmapi-as-a-code-sample.md)

