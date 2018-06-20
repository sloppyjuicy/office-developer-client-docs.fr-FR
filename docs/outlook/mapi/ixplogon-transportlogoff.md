---
title: IXPLogonTransportLogoff
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IXPLogon.TransportLogoff
api_type:
- COM
ms.assetid: b2b368ce-4486-4f90-985f-59e50ca95229
description: 'Derni�re modification�: samedi 23 juillet 2011'
ms.openlocfilehash: 195f2d718428eb8bb618fc982488c276d8a536da
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19784514"
---
# <a name="ixplogontransportlogoff"></a>IXPLogon::TransportLogoff

  
  
**S’applique à**: Outlook 
  
Lance le processus de fermeture de session. 
  
```cpp
HRESULT TransportLogoff(
  ULONG ulFlags
);
```

## <a name="parameters"></a>Param�tres

 _ulFlags_
  
> [in] R�serv� ; doit �tre �gal � z�ro.
    
## <a name="return-value"></a>Valeur renvoy�e

S_OK 
  
> L’appel a réussi et renvoyé la valeur attendue ou les valeurs. Si rien d’autre que S_OK est retourné, le fournisseur est déconnecté.
    
## <a name="remarks"></a>Remarques

Le spouleur MAPI appelle la méthode **IXPLogon::TransportLogoff** pour mettre fin à une session de fournisseur de transport pour un utilisateur particulier. Avant d’appeler **TransportLogoff**, le spouleur MAPI ignore les données sur les types d’adresse de messagerie pris en charge pour cette session passée dans la méthode [IXPLogon::AddressTypes](ixplogon-addresstypes.md) . 
  
## <a name="notes-to-implementers"></a>Remarques destinées aux responsables de l’implémentation

Le fournisseur de transport doit être préparé pour accepter un appel à **TransportLogoff** à tout moment. Si un message est en cours, le fournisseur doit arrêter le processus d’envoi. 
  
Le fournisseur de transport doit libérer toutes les ressources alloués pour la session en cours. Si elle a alloué de la mémoire pour cette session avec la fonction [MAPIAllocateBuffer](mapiallocatebuffer.md) , il doit libérer de la mémoire à l’aide de la fonction [MAPIFreeBuffer](mapifreebuffer.md) . Mémoire allouée par le fournisseur de transport pour répondre aux appels à la méthode [IXPLogon::AddressTypes](ixplogon-addresstypes.md) peut être annulée en toute sécurité à ce stade. 
  
En règle générale, sur la réalisation d’un appel **TransportLogoff** , un fournisseur doit tout d’abord invalider son objet d’ouverture de session en appelant la méthode [IMAPISupport::MakeInvalid](imapisupport-makeinvalid.md) , puis son objet prise en charge. L’implémentation du fournisseur de **TransportLogoff** doit libérer l’objet de prise en charge, car lorsque l’objet de prise en charge est lancé, le spouleur MAPI peut également libérer l’objet fournisseur lui-même. 
  
## <a name="see-also"></a>Voir aussi



[IMAPISupport::MakeInvalid](imapisupport-makeinvalid.md)
  
[IMAPISupport::SpoolerYield](imapisupport-spooleryield.md)
  
[IXPLogon::AddressTypes](ixplogon-addresstypes.md)
  
[MAPIAllocateBuffer](mapiallocatebuffer.md)
  
[MAPIFreeBuffer](mapifreebuffer.md)
  
[IXPLogon : IUnknown](ixplogoniunknown.md)

