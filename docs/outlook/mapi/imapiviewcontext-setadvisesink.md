---
title: IMAPIViewContextSetAdviseSink
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IMAPIViewContext.SetAdviseSink
api_type:
- COM
ms.assetid: 4799084a-b5d1-48c3-a889-b2f0e9d68c30
description: Dernière modification le 9 mars 2015
ms.openlocfilehash: 7ee641214e1eaae667af356fd8dbe51ff7dc7982
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33419393"
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
  
> [in] Pointeur vers un objet de type sink ou NULL de conseil de formulaire.
    
## <a name="return-value"></a>Valeur renvoyée

S_OK 
  
> L’inscription ou l’annulation de la notification de formulaire a réussi.
    
## <a name="remarks"></a>Remarques

Les objets form appellent la méthode **IMAPIViewContext::SetAdviseSink** pour s’inscrire afin d’en savoir plus sur les modifications apportées à la visionneuse de formulaires ou annuler une inscription préalable. Lorsque  _pmvns est_ définie sur NULL, le formulaire souhaite annuler une inscription. Lorsque  _pmvns_ pointe vers un formulaire de notification valide, le formulaire souhaite s’inscrire pour les notifications futures. 
  
## <a name="notes-to-implementers"></a>Remarques pour les responsables de l’implémentation

Lorsque **SetAdviseSink** inclut un pointeur de réception de notification de formulaire, conservez une référence à ce dernier jusqu’à ce qu’un autre appel **SetAdviseSink** soit effectué pour annuler la notification. Envoyez une notification lorsqu’une modification se produit dans votre visionneuse et lorsque vous chargez un nouveau message. 
  
Pour plus d’informations, voir [Envoyer et recevoir des notifications de formulaire.](sending-and-receiving-form-notifications.md)
  
## <a name="mfcmapi-reference"></a>Référence MFCMAPI

Pour voir un exemple de code MFCMAPI, consultez le tableau suivant.
  
|**Fichier**|**Fonction**|**Commentaire**|
|:-----|:-----|:-----|
|MyMAPIFormViewer.cpp  <br/> |CMyMAPIFormViewer::SetAdviseSink  <br/> |MFCMAPI implémente la **méthode IMAPIViewContext::SetAdviseSink** dans cette fonction.  <br/> |
   
## <a name="see-also"></a>Voir aussi



[MFCMAPI comme un exemple de Code](mfcmapi-as-a-code-sample.md)

