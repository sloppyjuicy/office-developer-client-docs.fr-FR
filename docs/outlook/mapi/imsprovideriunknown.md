---
title: IMSProvider IUnknown
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IMSProvider
api_type:
- COM
ms.assetid: 0f17aa44-abcb-4732-b013-d91652847cf6
description: Dernière modification le 9 mars 2015
ms.openlocfilehash: c5305ddd20b690f5c2e5807fb7ce2410549f7124
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33412862"
---
# <a name="imsprovider--iunknown"></a>IMSProvider : IUnknown

  
  
**S’applique à** : Outlook 2013 | Outlook 2016 
  
Permet d’accéder à un fournisseur de magasins de messages via un objet fournisseur de magasin de messages. Cet objet fournisseur de magasin de messages est renvoyé lors de l’ouverture de connecté du fournisseur par la fonction de point d’entrée [MSProviderInit](msproviderinit.md) du fournisseur de la boutique de messages. L’objet fournisseur de magasin de messages est principalement utilisé par les applications clientes et lepooler MAPI pour ouvrir les magasins de messages. 
  
|||
|:-----|:-----|
|Fichier d’en-tête :  <br/> |Mapispi.h  <br/> |
|Exposé par :  <br/> |Objets du fournisseur de banques de messages  <br/> |
|Implémenté par :  <br/> |Fournisseurs de magasins de messages  <br/> |
|Appelé par :  <br/> |MAPI et lepooler MAPI  <br/> |
|Identificateur d’interface :  <br/> |IID_IMSProvider  <br/> |
|Type de pointeur :  <br/> |LPMSPROVIDER  <br/> |
   
## <a name="vtable-order"></a>Ordre des vtables

|||
|:-----|:-----|
|[Arrêt](imsprovider-shutdown.md) <br/> |Ferme un fournisseur de magasins de messages de manière ordonnée.  <br/> |
|[Logon](imsprovider-logon.md) <br/> |Connecte MAPI à une instance d’un fournisseur de magasins de messages.  <br/> |
|[SpoolerLogon](imsprovider-spoolerlogon.md) <br/> |Connecte lepooler MAPI à une boutique de messages.  <br/> |
|[CompareStoreIDs](imsprovider-comparestoreids.md) <br/> |Compare deux identificateurs d’entrée de magasin de messages pour déterminer s’ils font référence au même objet store.  <br/> |
   
## <a name="remarks"></a>Remarques

MAPI utilise un objet fournisseur de magasin de messages par session, quel que soit le nombre de magasins de messages ouverts par le fournisseur de la boutique. Si une deuxième session MAPI se connecte à des magasins ouverts, MAPI appelle **MSProviderInit** une deuxième fois pour créer un objet fournisseur de magasin de messages à utiliser pour cette session. 
  
Un objet fournisseur de magasin de messages doit contenir les éléments suivants pour fonctionner correctement :
  
- Pointeur de routine d’allocation de mémoire  _lpMalloc_ à utiliser par tous les magasins ouverts à l’aide de cet objet fournisseur. 
    
- Les pointeurs de routine _lpfAllocateBuffer_, _ lpfAllocateMore _, et _lpfFreeBuffer_ pointent vers les fonctions d’allocation de mémoire [MAPIAllocateBuffer,](mapiallocatebuffer.md) [MAPIAllocateMore](mapiallocatemore.md)et [MAPIFreeBuffer.](mapifreebuffer.md) 
    
- Liste liée de toutes les magasins ouvertes à l’aide de cet objet fournisseur et pas encore fermées.
    
## <a name="see-also"></a>Voir aussi



[Interfaces MAPI](mapi-interfaces.md)

