---
title: IMSProvider IUnknown
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
api_name:
- IMSProvider
api_type:
- COM
ms.assetid: 0f17aa44-abcb-4732-b013-d91652847cf6
description: Dernière modification le 9 mars 2015
ms.openlocfilehash: e7eca6b089810424854565fbb6dc992afe48c94b
ms.sourcegitcommit: c0fae34cd3a9c75a7cffcf9ae8e417ddde07a989
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 02/12/2022
ms.locfileid: "62774873"
---
# <a name="imsprovider--iunknown"></a>IMSProvider : IUnknown

  
  
**S’applique à** : Outlook 2013 | Outlook 2016 
  
Permet d’accéder à un fournisseur de magasins de messages via un objet fournisseur de magasin de messages. Cet objet fournisseur de magasin de messages est renvoyé à l’ouverture de connecté du fournisseur par la fonction de point d’entrée [MSProviderInit](msproviderinit.md) du fournisseur de magasins de messages. L’objet fournisseur de magasin de messages est principalement utilisé par les applications clientes et lepooler MAPI pour ouvrir les magasins de messages. 
  
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
|[Arrêt](imsprovider-shutdown.md) <br/> |Ferme un fournisseur de magasins de messages de manière ordonnée. |
|[Logon](imsprovider-logon.md) <br/> |Connecte MAPI à une instance d’un fournisseur de magasins de messages. |
|[SpoolerLogon](imsprovider-spoolerlogon.md) <br/> |Connecte lepooler MAPI à une magasin de messages. |
|[CompareStoreIDs](imsprovider-comparestoreids.md) <br/> |Compare deux identificateurs d’entrée de magasin de messages pour déterminer s’ils font référence au même objet store. |
   
## <a name="remarks"></a>Remarques

MAPI utilise un objet fournisseur de magasin de messages par session, quel que soit le nombre de magasins de messages ouverts par le fournisseur de magasin. Si une deuxième session MAPI se connecte à des magasins ouverts, MAPI appelle **MSProviderInit** une deuxième fois pour créer un objet fournisseur de magasin de messages pour cette session à utiliser. 
  
Un objet fournisseur de magasin de messages doit contenir les éléments suivants pour fonctionner correctement :
  
- Pointeur de routine d’allocation de mémoire  _lpMalloc_ à utiliser par toutes les magasins ouverts à l’aide de cet objet fournisseur. 
    
- Les pointeurs de routine  _lpfAllocateBuffer_, _ lpfAllocateMore _, et  _lpfFreeBuffer_ vers les fonctions d’allocation de mémoire [MAPIAllocateBuffer](mapiallocatebuffer.md), [MAPIAllocateMore](mapiallocatemore.md) et [MAPIFreeBuffer](mapifreebuffer.md) . 
    
- Liste liée de toutes les magasins ouvertes à l’aide de cet objet fournisseur et pas encore fermées.
    
## <a name="see-also"></a>Voir aussi



[Interfaces MAPI](mapi-interfaces.md)

