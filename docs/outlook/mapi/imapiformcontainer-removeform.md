---
title: IMAPIFormContainerRemoveForm
description: Décrit la syntaxe, les paramètres, la valeur de retour et l’exemple de code d’IMAPIFormContainerRemoveForm, qui supprime un formulaire particulier d’un conteneur de formulaires.
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
api_name:
- IMAPIFormContainer.RemoveForm
api_type:
- COM
ms.assetid: 7f851ce8-bd01-4ea5-86e0-e44323cc0aab
ms.openlocfilehash: 2b20a15fdc153ee2e95eb0a3d54c970b71a90293
ms.sourcegitcommit: f872848fbeb5b2353179ad4bf4eab23f61f87666
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/01/2022
ms.locfileid: "65812206"
---
# <a name="imapiformcontainerremoveform"></a>IMAPIFormContainer::RemoveForm

  
  
**S’applique à** : Outlook 2013 | Outlook 2016 
  
Supprime un formulaire particulier d’un conteneur de formulaires.
  
```cpp
HRESULT RemoveForm(
  LPCSTR szMessageClass
);
```

## <a name="parameters"></a>Paramètres

 _szMessageClass_
  
> [in] Chaîne qui nomme la classe de message du formulaire à supprimer du conteneur de formulaires. Les noms de classes de message sont toujours des chaînes ANSI, jamais Unicode.
    
## <a name="return-value"></a>Valeur renvoyée

S_OK 
  
> L'appel a r�ussi et a renvoy� la valeur attendue ou les valeurs.
    
MAPI_E_NOT_FOUND 
  
> La classe de message passée dans le paramètre _szMessageClass_ ne correspond à la classe de message d’aucun formulaire du conteneur de formulaires. 
    
## <a name="mfcmapi-reference"></a>Référence MFCMAPI

Pour voir un exemple de code MFCMAPI, consultez le tableau suivant.
  
|**Fichier**|**Fonction**|**Commentaire**|
|:-----|:-----|:-----|
|FormContainerDlg.cpp  <br/> |CFormContainerDlg::OnDeleteSelectedItem  <br/> |MFCMAPI utilise la méthode **IMAPIFormContainer::RemoveForm** pour supprimer un formulaire d’un conteneur de formulaires. |
   
## <a name="see-also"></a>Voir aussi



[IMAPIFormContainer : IUnknown](imapiformcontaineriunknown.md)


[MFCMAPI comme un exemple de Code](mfcmapi-as-a-code-sample.md)

