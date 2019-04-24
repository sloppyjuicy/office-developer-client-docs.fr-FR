---
title: IMAPISupportCompleteMsg
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IMAPISupport.CompleteMsg
api_type:
- COM
ms.assetid: e7932433-abe0-4341-95e0-91b37c848145
description: 'Dernière modification : 23 juillet 2011'
ms.openlocfilehash: e8c52d71ee47966be09c6c0806eceafae0c5ff5b
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32331506"
---
# <a name="imapisupportcompletemsg"></a>IMAPISupport::CompleteMsg

  
  
**S’applique à** : Outlook 2013 | Outlook 2016 
  
Effectue un post-traitement sur un message. 
  
```cpp
HRESULT CompleteMsg(
  ULONG ulFlags,
  ULONG cbEntryID,
  LPENTRYID lpEntryID
);
```

## <a name="parameters"></a>Paramètres

 _ulFlags_
  
> [in] R�serv� ; doit �tre �gal � z�ro.
    
 _cbEntryID_
  
> dans Nombre d'octets dans l'identificateur d'entrée pointé par le paramètre _lpEntryID_ . 
    
 _lpEntryID_
  
> dans Pointeur vers l'identificateur d'entrée du message à traiter.
    
## <a name="return-value"></a>Valeur renvoyée

S_OK 
  
> Le post-traitement a réussi.
    
## <a name="remarks"></a>Remarques

La méthode **IMAPISupport:: CompleteMsg** est implémentée pour les objets de prise en charge du fournisseur de banque de messages et est appelée uniquement par les fournisseurs de banques de messages étroitement couplés avec les fournisseurs de transport. Les fournisseurs de magasins étroitement couplés appellent **IMAPISupport:: CompleteMsg** pour indiquer au spouleur MAPI d'postprocess un message. 
  
## <a name="notes-to-callers"></a>Remarques pour les appelants

Appeler **CompleteMsg** uniquement lorsque vous êtes fermement couplé à un fournisseur de transport, vous pouvez gérer tous les destinataires du message, et l'une des conditions suivantes existe: 
  
- Le message a été prétraité.
    
- Le message nécessite un post-traitement par le spouleur MAPI.
    
## <a name="see-also"></a>Voir aussi



[IMAPISupport : IUnknown](imapisupportiunknown.md)

