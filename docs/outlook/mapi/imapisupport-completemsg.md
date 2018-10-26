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
description: 'Derniére modification : samedi 23 juillet 2011'
ms.openlocfilehash: a948c8c25eec9b31735bb34b91e2dec4bca5fcfc
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/23/2018
ms.locfileid: "22583448"
---
# <a name="imapisupportcompletemsg"></a>IMAPISupport::CompleteMsg

  
  
**S’applique à** : Outlook 2013 | Outlook 2016 
  
Effectue post-traitement sur un message. 
  
```cpp
HRESULT CompleteMsg(
  ULONG ulFlags,
  ULONG cbEntryID,
  LPENTRYID lpEntryID
);
```

## <a name="parameters"></a>Param�tres

 _ulFlags_
  
> [in] R�serv� ; doit �tre �gal � z�ro.
    
 _cbEntryID_
  
> [in] Le nombre d’octets dans l’identificateur d’entrée indiqué par le paramètre _lpEntryID_ . 
    
 _lpEntryID_
  
> [in] Pointeur vers l’identificateur d’entrée du message à traiter.
    
## <a name="return-value"></a>Valeur renvoyée

S_OK 
  
> Le post-traitement a réussi.
    
## <a name="remarks"></a>Remarques

La méthode **IMAPISupport::CompleteMsg** est implémentée pour les objets de prise en charge de fournisseur de magasin de message et est appelée uniquement par les fournisseurs de magasins de message sont étroitement liés à des fournisseurs de transport. Fournisseurs de magasins étroitement couplés appellent **IMAPISupport::CompleteMsg** pour demander au spouleur MAPI de post-traitement d’un message. 
  
## <a name="notes-to-callers"></a>Notes aux appelants

Appelez **CompleteMsg** uniquement lorsque vous sont étroitement liés à un fournisseur de transport, vous pouvez gérer tous les destinataires du message et une des conditions suivantes existe : 
  
- Le message a été prétraité.
    
- Le message requiert post-traitement par le spouleur MAPI.
    
## <a name="see-also"></a>Voir aussi



[IMAPISupport : IUnknown](imapisupportiunknown.md)

