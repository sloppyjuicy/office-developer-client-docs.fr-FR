---
title: IMSProvider IUnknown
description: IMSProvider IUnknown fournit l’accès à un fournisseur de magasin de messages via un objet fournisseur de magasin de messages.
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
ms.openlocfilehash: e69f00b568e90c33c3b4657d654302b106aa2e2d
ms.sourcegitcommit: e2b79cc4469013a4b3705620a93aa70b88e6c996
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/02/2022
ms.locfileid: "65828545"
---
# <a name="imsprovider--iunknown"></a>IMSProvider : IUnknown

**S’applique à** : Outlook 2013 | Outlook 2016
  
Fournit l’accès à un fournisseur de magasin de messages par le biais d’un objet fournisseur de magasin de messages. Cet objet fournisseur de magasin de messages est retourné à l’ouverture de session du fournisseur par la fonction de point d’entrée [MSProviderInit](msproviderinit.md) du fournisseur de magasin de messages. L’objet fournisseur du magasin de messages est principalement utilisé par les applications clientes et le spouleur MAPI pour ouvrir des magasins de messages.
  
|Propriété|Valeur|
|:-----|:-----|
|Fichier d’en-tête :  <br/> |Mapispi.h  <br/> |
|Exposé par :  <br/> |Objets du fournisseur de banques de messages  <br/> |
|Implémenté par :  <br/> |Fournisseurs de magasins de messages  <br/> |
|Appelé par :  <br/> |MAPI et le spouleur MAPI  <br/> |
|Identificateur d’interface :  <br/> |IID_IMSProvider  <br/> |
|Type de pointeur :  <br/> |LPMSPROVIDER  <br/> |

## <a name="vtable-order"></a>Ordre des tables virtuelles

|Member|Description|
|:-----|:-----|
|[Arrêt](imsprovider-shutdown.md) <br/> |Ferme un fournisseur de magasin de messages de manière ordonnée. |
|[Logon](imsprovider-logon.md) <br/> |Connecte MAPI à une instance d’un fournisseur de magasin de messages. |
|[SpoolerLogon](imsprovider-spoolerlogon.md) <br/> |Enregistre le spouleur MAPI dans un magasin de messages. |
|[CompareStoreIDs](imsprovider-comparestoreids.md) <br/> |Compare deux identificateurs d’entrée de magasin de messages pour déterminer s’ils font référence au même objet de magasin. |

## <a name="remarks"></a>Remarques

MAPI utilise un objet fournisseur de magasin de messages par session, quel que soit le nombre de magasins de messages ouverts par le fournisseur du magasin. Si une deuxième session MAPI se connecte à des magasins ouverts, MAPI appelle **MSProviderInit** une deuxième fois pour créer un objet fournisseur de magasin de messages à utiliser pour cette session.
  
Un objet fournisseur de magasin de messages doit contenir les éléments suivants pour fonctionner correctement :
  
- Pointeur de routine d’allocation de mémoire _lpMalloc_ à utiliser par tous les magasins ouverts à l’aide de cet objet fournisseur.
- Les pointeurs de routine _lpfAllocateBuffer_, _lpfAllocateMore_ et _lpfFreeBuffer_ vers les fonctions d’allocation de mémoire [MAPIAllocateBuffer](mapiallocatebuffer.md), [MAPIAllocateMore](mapiallocatemore.md) et [MAPIFreeBuffer](mapifreebuffer.md) .
- Liste liée de tous les magasins ouverts à l’aide de cet objet fournisseur et non encore fermés.

## <a name="see-also"></a>Voir aussi

[Interfaces MAPI](mapi-interfaces.md)
