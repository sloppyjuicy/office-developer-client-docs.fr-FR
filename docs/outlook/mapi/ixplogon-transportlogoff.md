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
description: 'Dernière modification : 23 juillet 2011'
ms.openlocfilehash: 78b4feeca263035b9c90184f10edd294e6cd7b10
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32351582"
---
# <a name="ixplogontransportlogoff"></a>IXPLogon::TransportLogoff

  
  
**S’applique à** : Outlook 2013 | Outlook 2016 
  
Lance le processus de fermeture de session. 
  
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
  
> L'appel a réussi et a renvoyé la ou les valeurs attendues. Si un élément autre que S_OK est renvoyé, le fournisseur est déconnecté.
    
## <a name="remarks"></a>Remarques

Le spouleur MAPI appelle la méthode **IXPLogon:: TransportLogoff** pour mettre fin à une session de fournisseur de transport pour un utilisateur particulier. Avant d'appeler **TransportLogoff**, le spouleur MAPI ignore les données relatives aux types d'adresses de messagerie pris en charge pour cette session passée dans la méthode [IXPLogon:: AddressTypes](ixplogon-addresstypes.md) . 
  
## <a name="notes-to-implementers"></a>Remarques pour les responsables de l’implémentation

Le fournisseur de transport doit être prêt à accepter un appel à **TransportLogoff** à tout moment. Si un message est en cours d'opération, le fournisseur doit arrêter le processus d'envoi. 
  
Le fournisseur de transport doit libérer toutes les ressources allouées pour sa session actuelle. Si elle a alloué de la mémoire pour cette session à l'aide de la fonction [MAPIAllocateBuffer](mapiallocatebuffer.md) , elle doit libérer la mémoire à l'aide de la fonction [MAPIFreeBuffer](mapifreebuffer.md) . Toute mémoire allouée par le fournisseur de transport pour satisfaire les appels à la méthode [IXPLogon:: AddressTypes](ixplogon-addresstypes.md) peut être publiée en toute sécurité. 
  
En règle générale, lors de l'exécution d'un appel **TransportLogoff** , un fournisseur doit d'abord invalider son objet Logon en appelant la méthode [IMAPISupport:: MakeInvalid](imapisupport-makeinvalid.md) , puis libérer son objet support. L'implémentation du fournisseur de **TransportLogoff** doit libérer le dernier objet de prise en charge, car lorsque l'objet de support est publié, le spouleur MAPI peut également libérer l'objet fournisseur lui-même. 
  
## <a name="see-also"></a>Voir aussi



[IMAPISupport::MakeInvalid](imapisupport-makeinvalid.md)
  
[IMAPISupport::SpoolerYield](imapisupport-spooleryield.md)
  
[IXPLogon::AddressTypes](ixplogon-addresstypes.md)
  
[MAPIAllocateBuffer](mapiallocatebuffer.md)
  
[MAPIFreeBuffer](mapifreebuffer.md)
  
[IXPLogon : IUnknown](ixplogoniunknown.md)

