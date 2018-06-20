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
description: 'Derni�re modification�: lundi 9 mars 2015'
ms.openlocfilehash: abee768dd29cc807b605a7d13570a579cb271b2c
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19784119"
---
# <a name="imapiviewcontextsetadvisesink"></a>IMAPIViewContext::SetAdviseSink

  
  
**S’applique à**: Outlook 
  
Gère l’inscription d’un formulaire pour recevoir des notifications sur les modifications dans la visionneuse. 
  
```cpp
HRESULT SetAdviseSink(
LPMAPIFORMADVISESINK pmvns
);
```

## <a name="parameters"></a>Paramètres

 _pmvns_
  
> [in] Pointeur vers un formulaire de notification objet récepteur ou NULL.
    
## <a name="return-value"></a>Valeur renvoy�e

S_OK 
  
> L’inscription ou l’annulation de la notification de formulaire a réussi.
    
## <a name="remarks"></a>Remarques

Objets de formulaire appeler la méthode de **IMAPIViewContext::SetAdviseSink** pouvez en savoir plus sur les modifications dans la visionneuse de formulaire ou d’annuler une inscription préalable. Lorsque _pmvns_ est défini sur NULL, le formulaire souhaite annuler un enregistrement. Lorsque le récepteur de notification de points _pmvns_ à un formulaire valid, le formulaire souhaite enregistrer les notifications ultérieures. 
  
## <a name="notes-to-implementers"></a>Remarques destinées aux responsables de l’implémentation

Lorsque **SetAdviseSink** comprend un formulaire pointeur du récepteur de notification, conserver une référence à celui-ci jusqu'à ce qu’un autre appel **SetAdviseSink** est effectué pour annuler la notification. Envoyer une notification lorsque cet événement se produit une modification dans votre visionneuse et lors du chargement d’un nouveau message. 
  
Pour plus d’informations, consultez [envoi et réception des Notifications](sending-and-receiving-form-notifications.md).
  
## <a name="mfcmapi-reference"></a>Référence MFCMAPI

Pour des exemples de code MFCMAPI, voir le tableau suivant.
  
|**Fichier**|**Fonction**|**Commentaire**|
|:-----|:-----|:-----|
|MyMAPIFormViewer.cpp  <br/> |CMyMAPIFormViewer::SetAdviseSink  <br/> |MFCMAPI implémente la méthode **IMAPIViewContext::SetAdviseSink** dans cette fonction.  <br/> |
   
## <a name="see-also"></a>Voir aussi



[MFCMAPI comme un exemple de Code](mfcmapi-as-a-code-sample.md)

