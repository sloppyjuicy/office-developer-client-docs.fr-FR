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
description: 'Derni�re modification�: lundi 9 mars 2015'
ms.openlocfilehash: 994041d050df56fd3fa3c0e599542e05a202ad65
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32329427"
---
# <a name="imapiformcontainergetdisplay"></a>IMAPIFormContainer::GetDisplay

  
  
**S’applique à** : Outlook 2013 | Outlook 2016 
  
Renvoie le nom d'affichage d'un conteneur de formulaire.
  
```cpp
HRESULT GetDisplay(
  ULONG ulFlags,
  LPSTR FAR * pszDisplayName
);
```

## <a name="parameters"></a>Paramètres

 _ulFlags_
  
> dans Masque de des indicateurs qui contrôle le type de la chaîne renvoyée. L'indicateur suivant peut être défini:
    
MAPI_UNICODE 
  
> La chaîne renvoyée est au format Unicode. Si l'indicateur MAPI_UNICODE n'est pas défini, la chaîne est au format ANSI.
    
 _pszDisplayName_
  
> remarquer Pointeur vers une chaîne qui contient le nom complet du conteneur de formulaire.
    
## <a name="return-value"></a>Valeur renvoyée

S_OK 
  
> L'appel a r�ussi et a renvoy� la valeur attendue ou les valeurs.
    
## <a name="mfcmapi-reference"></a>Référence MFCMAPI

Pour voir un exemple de code MFCMAPI, consultez le tableau suivant.
  
|**Fichier**|**Fonction**|**Commentaire**|
|:-----|:-----|:-----|
|FormContainerDlg. cpp  <br/> |CFormContainerDlg:: CFormContainerDlg  <br/> |MFCMAPI utilise la méthode **IMAPIFormContainer:: GetDisplay** pour obtenir le nom du conteneur de formulaire lorsqu'il restitue CFormContainerDlg.  <br/> |
   
## <a name="see-also"></a>Voir aussi



[IMAPIFormContainer : IUnknown](imapiformcontaineriunknown.md)


[MFCMAPI comme un exemple de Code](mfcmapi-as-a-code-sample.md)

