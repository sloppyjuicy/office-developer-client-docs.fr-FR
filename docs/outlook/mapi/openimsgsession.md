---
title: OpenIMsgSession
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.OpenIMsgSession
api_type:
- COM
ms.assetid: f75229e3-5f44-4298-8706-9eddf0ef124c
description: 'Derni�re modification�: lundi 9 mars 2015'
ms.openlocfilehash: e7f652e7426792d8b4c878b7f6738439aec65348
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19784927"
---
# <a name="openimsgsession"></a>OpenIMsgSession

  
  
**S’applique à**: Outlook 
  
Crée et ouvre une session de messagerie qui regroupe les messages créés qu’il contient. 
  
|||
|:-----|:-----|
|Fichier d’en-tête :  <br/> |IMessage.h  <br/> |
|Implémentée par :  <br/> |MAPI  <br/> |
|Appelée par :  <br/> |Les applications clientes et des fournisseurs de services  <br/> |
   
```cpp
SCODE OpenIMsgSession(
  LPMALLOC lpMalloc,
  ULONG ulFlags,
  LPMSGSESS FAR * lppMsgSess
);
```

## <a name="parameters"></a>Paramètres

 _lpMalloc_
  
> [in] Pointeur vers un objet d’allocation mémoire exposant l’interface OLE [IMalloc](http://msdn.microsoft.com/library/047f281e-2665-4d6d-9a0b-918cd3339447%28Office.15%29.aspx) . MAPI doit utiliser cette méthode de répartition lorsque vous travaillez avec l’interface OLE [IStorage](http://msdn.microsoft.com/library/stg.istorage%28Office.15%29.aspx) . 
    
 _ulFlags_
  
> [in] R�serv� ; doit �tre �gal � z�ro. 
    
 _lppMsgSess_
  
> [out] Pointeur vers un pointeur vers l’objet de session message renvoyé.
    
## <a name="return-value"></a>Valeur renvoy�e

S_OK
  
> La session a été ouvert.
    
MAPI_E_INVALID_PARAMETER
  
>  _lpMalloc_ ou _lppMsgSess_ est NULL. 
    
MAPI_E_INVALID_FLAGS
  
> Indicateurs non valides ont été transmis.
    
MAPI_UNICODE
  
> Lorsque vous appelez cette fonction, un client ou fournisseur de services définit l’indicateur MAPI_UNICODE pour créer les fichiers .msg Unicode. Le fichier [Imessage](imessageimapiprop.md) affiche STORE_UNICODE_OK dans son PR_STORE_SUPPORT_MASK et prend en charge les propriétés Unicode. 
    
## <a name="remarks"></a>Remarques

Une session de messagerie est utilisée par les applications clientes et fournisseurs de services pour gérer les problèmes liés à plusieurs concernant MAPI [IMessage : IMAPIProp](imessageimapiprop.md) objets greffées sur des objets OLE **IStorage** sous-jacents. Le client ou le fournisseur utilise les fonctions **OpenIMsgSession** et [CloseIMsgSession](closeimsgsession.md) pour encapsuler la création de ces messages à l’intérieur d’une session de messagerie. Une fois la session de messagerie est ouvert, le client ou le fournisseur lui passe un pointeur dans un appel à [OpenIMsgOnIStg](openimsgonistg.md) pour créer un nouveau **IMessage**- sur - objet **IStorage** . 
  
Enregistre une session de messagerie de tous les **IMessage**- sur - objets **IStorage** créés pendant la durée de la session, en plus de toutes les pièces jointes et d’autres propriétés des messages. Lorsqu’un client ou un fournisseur appelle **CloseIMsgSession**, il ferme tous ces objets. L’appel de **CloseIMsgSession** est la seule façon de fermer **IMessage**- sur - objets **IStorage** . 
  
 **OpenIMsgSession** est utilisé par les clients et les fournisseurs qui requièrent la possibilité de gérer plusieurs messages connexes en tant qu’objets OLE **IStorage** . Si seule un des messages doit être ouvert à la fois, il n’est pas nécessaire pour effectuer le suivi de plusieurs messages et aucune raison de créer une session de messagerie avec **OpenIMsgSession**. 
  
Car elle porte sur un objet OLE sous-jacent, MAPI doit utiliser l’allocation de mémoire OLE. Pour plus d’informations sur les objets de stockage structuré OLE et l’allocation de mémoire OLE, consultez [OLE et transfert de données](http://msdn.microsoft.com/library/d4a57956-37ba-44ca-8efc-bf617ad5e77b.aspx). 
  

