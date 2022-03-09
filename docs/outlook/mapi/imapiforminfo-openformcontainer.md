---
title: IMAPIFormInfoOpenFormContainer
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
api_name:
- IMAPIFormInfo.OpenFormContainer
api_type:
- COM
ms.assetid: 1d6eec99-59f9-4700-9b83-7f7f8787a9f8
ms.openlocfilehash: 8f16cf47567adb109e9acd9136102044b163be9d
ms.sourcegitcommit: 518845d053a009b11c8d907a33822161c0b6bc96
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/08/2022
ms.locfileid: "63373143"
---
# <a name="imapiforminfoopenformcontainer"></a>IMAPIFormInfo::OpenFormContainer

  
  
**S’applique à** : Outlook 2013 | Outlook 2016 
  
Renvoie un pointeur vers le conteneur de formulaire dans lequel un formulaire particulier est installé.
  
```cpp
HRESULT OpenFormContainer(
  LPMAPIFORMCONTAINER FAR * ppformcontainer
);
```

## <a name="parameters"></a>Paramètres

 _ppformcontainer_
  
> [out] Pointeur vers un pointeur vers l’objet conteneur de formulaire renvoyé.
    
## <a name="return-value"></a>Valeur renvoyée

S_OK 
  
> L'appel a r�ussi et a renvoy� la valeur attendue ou les valeurs.
    
## <a name="see-also"></a>Voir aussi



[IMAPIFormInfo : IMAPIProp](imapiforminfoimapiprop.md)

