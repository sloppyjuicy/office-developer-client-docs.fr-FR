---
title: IMAPIFormContainerRemoveForm
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IMAPIFormContainer.RemoveForm
api_type:
- COM
ms.assetid: 7f851ce8-bd01-4ea5-86e0-e44323cc0aab
description: 'Derni�re modification�: lundi 9 mars 2015'
ms.openlocfilehash: e53c0cbd9946ff04516594a7ce99fdc2daf4ff4d
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32355741"
---
# <a name="imapiformcontainerremoveform"></a>IMAPIFormContainer::RemoveForm

  
  
**S’applique à** : Outlook 2013 | Outlook 2016 
  
Supprime un formulaire particulier d'un conteneur de formulaires.
  
```cpp
HRESULT RemoveForm(
  LPCSTR szMessageClass
);
```

## <a name="parameters"></a>Paramètres

 _szMessageClass_
  
> dans Chaîne qui nomme la classe de message du formulaire à supprimer du conteneur de formulaire. Les noms de classe de message sont toujours des chaînes ANSI, jamais Unicode.
    
## <a name="return-value"></a>Valeur renvoyée

S_OK 
  
> L'appel a r�ussi et a renvoy� la valeur attendue ou les valeurs.
    
MAPI_E_NOT_FOUND 
  
> La classe de message passée dans le paramètre _szMessageClass_ ne correspond pas à la classe de message d'un formulaire dans le conteneur de formulaire. 
    
## <a name="mfcmapi-reference"></a>Référence MFCMAPI

Pour voir un exemple de code MFCMAPI, consultez le tableau suivant.
  
|**Fichier**|**Fonction**|**Commentaire**|
|:-----|:-----|:-----|
|FormContainerDlg. cpp  <br/> |CFormContainerDlg:: OnDeleteSelectedItem  <br/> |MFCMAPI utilise la méthode **IMAPIFormContainer:: RemoveForm** pour supprimer un formulaire d'un conteneur de formulaire.  <br/> |
   
## <a name="see-also"></a>Voir aussi



[IMAPIFormContainer : IUnknown](imapiformcontaineriunknown.md)


[MFCMAPI comme un exemple de Code](mfcmapi-as-a-code-sample.md)

