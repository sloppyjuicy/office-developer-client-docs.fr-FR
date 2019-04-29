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
  
Permet d'accéder à un fournisseur de banque de messages par le biais d'un objet fournisseur de banque de messages. Cet objet fournisseur de banque de messages est renvoyé lors de l'ouverture de session du fournisseur par la fonction de point d'entrée [MSProviderInit](msproviderinit.md) du fournisseur de banque de messages. L'objet fournisseur de banque de messages est principalement utilisé par les applications clientes et le spouleur MAPI pour ouvrir les banques de messages. 
  
|||
|:-----|:-----|
|Fichier d’en-tête :  <br/> |Mapispi. h  <br/> |
|Exposé par:  <br/> |Objets du fournisseur de banques de messages  <br/> |
|Implémenté par :  <br/> |Fournisseurs de banques de messages  <br/> |
|Appelé par :  <br/> |MAPI et spouleur MAPI  <br/> |
|Identificateur de l'interface:  <br/> |IID_IMSProvider  <br/> |
|Type de pointeur:  <br/> |LPMSPROVIDER  <br/> |
   
## <a name="vtable-order"></a>Ordre vtable

|||
|:-----|:-----|
|[Arrêt](imsprovider-shutdown.md) <br/> |Ferme un fournisseur de banque de messages de manière ordonnée.  <br/> |
|[Logon](imsprovider-logon.md) <br/> |Journalise MAPI sur une instance d'un fournisseur de banque de messages.  <br/> |
|[SpoolerLogon](imsprovider-spoolerlogon.md) <br/> |Enregistre le spouleur MAPI sur une banque de messages.  <br/> |
|[CompareStoreIDs](imsprovider-comparestoreids.md) <br/> |Compare deux identificateurs d'entrée de banque de messages pour déterminer s'ils font référence au même objet Store.  <br/> |
   
## <a name="remarks"></a>Remarques

MAPI utilise un seul objet fournisseur de banque de messages par session, quel que soit le nombre de banques de messages ouvertes par le fournisseur de banque d'informations. Si une deuxième session MAPI se connecte à des magasins ouverts, MAPI appelle **MSProviderInit** une deuxième fois pour créer un nouvel objet fournisseur de banque de messages pour cette session. 
  
Pour fonctionner correctement, un objet fournisseur de banque de messages doit contenir les éléments suivants:
  
- Pointeur de routine d'allocation de mémoire _lpMalloc_ pour une utilisation par tous les magasins ouverts à l'aide de cet objet fournisseur. 
    
- Les pointeurs de routine _lpfAllocateBuffer_, _ lpfAllocateMore _ et _lpfFreeBuffer_ vers les fonctions d'allocation de mémoire [MAPIAllocateBuffer](mapiallocatebuffer.md), [MAPIAllocateMore](mapiallocatemore.md)et [MAPIFreeBuffer](mapifreebuffer.md) . 
    
- Liste liée de tous les magasins ouverts à l'aide de cet objet fournisseur et non encore fermés.
    
## <a name="see-also"></a>Voir aussi



[Interfaces MAPI](mapi-interfaces.md)

