---
title: IMAPIViewContextSetAdviseSink
description: IMAPIViewContext SetAdviseSink gère l’inscription d’un formulaire pour recevoir des notifications sur les modifications apportées à la visionneuse.
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
api_name:
- IMAPIViewContext.SetAdviseSink
api_type:
- COM
ms.assetid: 4799084a-b5d1-48c3-a889-b2f0e9d68c30
ms.openlocfilehash: c97dd21351b8bbe87524e673197e850d18b06018
ms.sourcegitcommit: e2b79cc4469013a4b3705620a93aa70b88e6c996
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/02/2022
ms.locfileid: "65827764"
---
# <a name="imapiviewcontextsetadvisesink"></a>IMAPIViewContext::SetAdviseSink

  
  
**S’applique à** : Outlook 2013 | Outlook 2016 
  
Gère l’inscription d’un formulaire pour recevoir des notifications sur les modifications apportées à la visionneuse. 
  
```cpp
HRESULT SetAdviseSink(
LPMAPIFORMADVISESINK pmvns
);
```

## <a name="parameters"></a>Paramètres

 _pmvns_
  
> [in] Pointeur vers un objet récepteur conseiller de formulaire ou NULL.
    
## <a name="return-value"></a>Valeur renvoyée

S_OK 
  
> L’inscription ou l’annulation de la notification de formulaire a réussi.
    
## <a name="remarks"></a>Remarques

Les objets de formulaire appellent la méthode **IMAPIViewContext::SetAdviseSink** pour s’inscrire pour en savoir plus sur les modifications apportées à la visionneuse de formulaires ou annuler une inscription précédente. Lorsque  _pmvns_ est défini sur NULL, le formulaire souhaite annuler une inscription. Lorsque  _pmvns_ pointe vers un récepteur de conseils de formulaire valide, le formulaire souhaite s’inscrire pour les notifications futures. 
  
## <a name="notes-to-implementers"></a>Remarques pour les responsables de l’implémentation

Lorsque **SetAdviseSink** inclut un pointeur récepteur de conseil de formulaire, conservez une référence à celui-ci jusqu’à ce qu’un autre appel **SetAdviseSink** soit effectué pour annuler la notification. Envoyez une notification lorsqu’une modification se produit dans votre visionneuse et lorsque vous chargez un nouveau message. 
  
Pour plus d’informations, consultez [Envoi et réception de notifications de formulaire](sending-and-receiving-form-notifications.md).
  
## <a name="mfcmapi-reference"></a>Référence MFCMAPI

Pour voir un exemple de code MFCMAPI, consultez le tableau suivant.
  
|**Fichier**|**Fonction**|**Commentaire**|
|:-----|:-----|:-----|
|MyMAPIFormViewer.cpp  <br/> |CMyMAPIFormViewer::SetAdviseSink  <br/> |MFCMAPI implémente la méthode **IMAPIViewContext::SetAdviseSink** dans cette fonction. |
   
## <a name="see-also"></a>Voir aussi



[MFCMAPI comme un exemple de Code](mfcmapi-as-a-code-sample.md)

