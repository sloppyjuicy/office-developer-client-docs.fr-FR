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
ms.openlocfilehash: e8c52d71ee47966be09c6c0806eceafae0c5ff5b
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33411189"
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
  
> [in] Nombre d’bytes dans l’identificateur d’entrée pointé par _le paramètre lpEntryID._ 
    
 _lpEntryID_
  
> [in] Pointeur vers l’identificateur d’entrée du message à traiter.
    
## <a name="return-value"></a>Valeur renvoyée

S_OK 
  
> Le post-traitement a réussi.
    
## <a name="remarks"></a>Remarques

La **méthode IMAPISupport::CompleteMsg** est implémentée pour les objets de prise en charge des fournisseurs de magasins de messages et est appelée uniquement par les fournisseurs de magasins de messages étroitement associés aux fournisseurs de transport. Les fournisseurs de magasins étroitement couplés appellent **IMAPISupport::CompleteMsg** pour demander aupooler MAPI de postprocesser un message. 
  
## <a name="notes-to-callers"></a>Remarques pour les appelants

Appelez **CompleteMsg** uniquement lorsque vous êtes étroitement associé à un fournisseur de transport, vous pouvez gérer tous les destinataires du message et l’une des conditions suivantes existe : 
  
- Le message a été prétraité.
    
- Le message nécessite un post-traitement par lepooler MAPI.
    
## <a name="see-also"></a>Voir aussi



[IMAPISupport : IUnknown](imapisupportiunknown.md)

