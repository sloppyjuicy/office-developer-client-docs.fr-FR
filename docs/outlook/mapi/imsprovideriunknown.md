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
description: Dernière modification le 09 mars 2015
ms.openlocfilehash: 1c00e54d02ba494c94c9826eabe142e1bd3b9a80
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/23/2018
ms.locfileid: "22579626"
---
# <a name="imsprovider--iunknown"></a>IMSProvider : IUnknown

  
  
**S’applique à**: Outlook 2013 | Outlook 2016 
  
Permet d’accéder à un fournisseur de magasin de message via un objet de fournisseur de magasin de message. Cet objet de fournisseur de magasin de message est renvoyé à la connexion au fournisseur en fonction du point d’entrée [MSProviderInit](msproviderinit.md) du fournisseur de banque de messages. L’objet de fournisseur de banque de messages est principalement utilisé par les applications clientes et le spouleur MAPI pour ouvrir les banques de messages. 
  
|||
|:-----|:-----|
|Fichier d’en-tête :  <br/> |Mapispi.h  <br/> |
|Exposés par :  <br/> |Objets du fournisseur de banque de messages  <br/> |
|Implémentée par :  <br/> |Fournisseurs de banque de messages  <br/> |
|Appelée par :  <br/> |MAPI et le spouleur MAPI  <br/> |
|Identificateur de l’interface :  <br/> |IID_IMSProvider  <br/> |
|Type de pointeur :  <br/> |LPMSPROVIDER  <br/> |
   
## <a name="vtable-order"></a>Ordre vtable

|||
|:-----|:-----|
|[Arrêt](imsprovider-shutdown.md) <br/> |Ferme un fournisseur de magasin de message de manière ordonnée.  <br/> |
|[Logon](imsprovider-logon.md) <br/> |Journaux MAPI sur une instance d’un fournisseur de magasin de message.  <br/> |
|[SpoolerLogon](imsprovider-spoolerlogon.md) <br/> |Enregistre le spouleur MAPI sur une banque de messages.  <br/> |
|[CompareStoreIDs](imsprovider-comparestoreids.md) <br/> |Compare deux messages magasin identificateurs d’entrée pour déterminer si elles font référence au même objet store.  <br/> |
   
## <a name="remarks"></a>Remarques

MAPI utilise un objet de fournisseur de magasins de message par session, quel que soit le nombre de messages ouverts par le fournisseur de magasin de magasins. Si un deuxième MAPI session se connecte à tous les magasins, appels MAPI **MSProviderInit** une deuxième fois pour créer un nouvel objet de fournisseur de magasin de message pour cette session à utiliser. 
  
Un objet de fournisseur de magasin de message doit contenir ce qui suit pour fonctionner correctement :
  
- _LpMalloc_ allocation de mémoire routine pointeur de pour une utilisation par tous les magasins ouvert à l’aide de l’objet de ce fournisseur. 
    
- Le _lpfAllocateBuffer_, _ lpfAllocateMore _, ainsi que des pointeurs routine _lpfFreeBuffer_ pour les fonctions d’allocation de mémoire [MAPIAllocateBuffer](mapiallocatebuffer.md), [MAPIAllocateMore](mapiallocatemore.md)et [MAPIFreeBuffer](mapifreebuffer.md) . 
    
- Une liste de toutes les banques liée ouvert à l’aide de cet objet de fournisseur et n’est pas encore fermé.
    
## <a name="see-also"></a>Voir aussi



[Interfaces MAPI](mapi-interfaces.md)

