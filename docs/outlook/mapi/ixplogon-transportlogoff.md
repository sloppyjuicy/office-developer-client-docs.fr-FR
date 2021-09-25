---
title: IXPLogonTransportLogoff
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
api_name:
- IXPLogon.TransportLogoff
api_type:
- COM
ms.assetid: b2b368ce-4486-4f90-985f-59e50ca95229
description: 'Derniére modification : samedi 23 juillet 2011'
ms.openlocfilehash: 06832b3ae760983474fd3553324fee304bd9ac37
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/24/2021
ms.locfileid: "59595930"
---
# <a name="ixplogontransportlogoff"></a>IXPLogon::TransportLogoff

  
  
**S’applique à** : Outlook 2013 | Outlook 2016 
  
Lance le processus de ffage de logo. 
  
```cpp
HRESULT TransportLogoff(
  ULONG ulFlags
);
```

## <a name="parameters"></a>Paramètres

 _ulFlags_
  
> [in] R�serv� ; doit �tre �gal � z�ro.
    
## <a name="return-value"></a>Valeur renvoyée

S_OK 
  
> L’appel a réussi et a renvoyé la ou les valeurs attendues. Si une autre S_OK est renvoyée, le fournisseur est déconnecté.
    
## <a name="remarks"></a>Remarques

Lepooler MAPI appelle la méthode **IXPLogon::TransportLogoff** pour mettre fin à une session de fournisseur de transport pour un utilisateur particulier. Avant **d’appeler TransportLogoff,** lepooler MAPI rejette toutes les données sur les types d’adresses de messagerie pris en charge pour cette session transmises dans la méthode [IXPLogon::AddressTypes.](ixplogon-addresstypes.md) 
  
## <a name="notes-to-implementers"></a>Remarques pour les responsables de l’implémentation

Le fournisseur de transport doit être prêt à accepter un appel à **TransportLogoff** à tout moment. Si un message est en cours, le fournisseur doit arrêter le processus d’envoi. 
  
Le fournisseur de transport doit libérer toutes les ressources allouées pour sa session en cours. Si elle a alloué de la mémoire pour cette session avec la fonction [MAPIAllocateBuffer,](mapiallocatebuffer.md) elle doit libérer de la mémoire à l’aide de la fonction [MAPIFreeBuffer.](mapifreebuffer.md) Toute mémoire allouée par le fournisseur de transport pour satisfaire les appels à la méthode [IXPLogon::AddressTypes](ixplogon-addresstypes.md) peut être libérée en toute sécurité pour le moment. 
  
En règle générale, lors de l’exécution d’un appel **TransportLogoff,** un fournisseur doit d’abord invalider son objet d’accès en appelant la méthode [IMAPISupport::MakeInvalid,](imapisupport-makeinvalid.md) puis libérer son objet de support. L’implémentation du fournisseur de **TransportLogoff** doit libérer l’objet de support en dernier, car lorsque l’objet de support est libéré, lepooler MAPI peut également libérer l’objet fournisseur lui-même. 
  
## <a name="see-also"></a>Voir aussi



[IMAPISupport::MakeInvalid](imapisupport-makeinvalid.md)
  
[IMAPISupport::SpoolerYield](imapisupport-spooleryield.md)
  
[IXPLogon::AddressTypes](ixplogon-addresstypes.md)
  
[MAPIAllocateBuffer](mapiallocatebuffer.md)
  
[MAPIFreeBuffer](mapifreebuffer.md)
  
[IXPLogon : IUnknown](ixplogoniunknown.md)

