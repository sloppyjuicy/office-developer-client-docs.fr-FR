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
ms.openlocfilehash: 607105bd58a14a3510f1ae71246069440a4f05cb
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32326193"
---
# <a name="openimsgsession"></a>OpenIMsgSession

  
  
**S’applique à** : Outlook 2013 | Outlook 2016 
  
Crée et ouvre une session de message qui regroupe les messages créés dans celui-ci. 
  
|||
|:-----|:-----|
|Fichier d’en-tête :  <br/> |IMessage. h  <br/> |
|Implémenté par :  <br/> |MAPI  <br/> |
|Appelé par :  <br/> |Applications clientes et fournisseurs de services  <br/> |
   
```cpp
SCODE OpenIMsgSession(
  LPMALLOC lpMalloc,
  ULONG ulFlags,
  LPMSGSESS FAR * lppMsgSess
);
```

## <a name="parameters"></a>Paramètres

 _lpMalloc_
  
> dans Pointeur vers un objet de l'allocation de mémoire qui expose [](https://docs.microsoft.com/windows/desktop/api/objidl/nn-objidl-imalloc) l'interface OLE imalloc. MAPI doit utiliser cette méthode d'allocation lorsque vous utilisez l'interface OLE [IStorage](https://docs.microsoft.com/windows/desktop/api/objidl/nn-objidl-istorage) . 
    
 _ulFlags_
  
> [in] R�serv� ; doit �tre �gal � z�ro. 
    
 _lppMsgSess_
  
> remarquer Pointeur vers un pointeur vers l'objet de session de message renvoyé.
    
## <a name="return-value"></a>Valeur renvoyée

S_OK
  
> La session a été ouverte.
    
MAPI_E_INVALID_PARAMETER
  
>  _lpMalloc_ ou _lppMsgSess_ est null. 
    
MAPI_E_INVALID_FLAGS
  
> Des indicateurs non valides ont été transmis.
    
MAPI_UNICODE
  
> Lors de l'appel de cette fonction, un client ou un fournisseur de services définit l'indicateur MAPI_UNICODE pour créer des fichiers. MSG Unicode. Le fichier [IMessage](imessageimapiprop.md) obtenu affiche STORE_UNICODE_OK dans son PR_STORE_SUPPORT_MASK et prend en charge les propriétés Unicode. 
    
## <a name="remarks"></a>Remarques

Une session de message est utilisée par les applications clientes et les fournisseurs de services qui souhaitent traiter avec plusieurs objets de la fonction IMessage MAPI associés [: IMAPIProp](imessageimapiprop.md) objets construits sur des objets OLE **IStorage** sous-jacents. Le client ou le fournisseur utilise les fonctions **OpenIMsgSession** et [CloseIMsgSession](closeimsgsession.md) pour encapsuler la création de ces messages à l'intérieur d'une session de message. Une fois la session de message ouverte, le client ou le fournisseur lui transmet un pointeur dans un appel à [OpenIMsgOnIStg](openimsgonistg.md) pour créer un nouvel objet **IMessage**sur l' **IStorage** . 
  
Une session de message assure le suivi de tous les objets **IMessage**sur le **IStorage** créés pendant la durée de la session, en plus de toutes les pièces jointes et d'autres propriétés des messages. Lorsqu'un client ou un fournisseur appelle **CloseIMsgSession**, il ferme tous ces objets. L'appel de **CloseIMsgSession** est la seule façon de fermer des objets **IMessage**-sur- **IStorage** . 
  
 **OpenIMsgSession** est utilisé par les clients et les fournisseurs qui ont besoin de pouvoir gérer plusieurs messages connexes en tant qu'objets **IStorage** OLE. Si un seul de ces messages doit être ouvert à la fois, il n'est pas nécessaire de suivre plusieurs messages et aucune raison de créer une session de message avec **OpenIMsgSession**. 
  
Étant donné qu'il s'agit d'un objet OLE sous-jacent, MAPI doit utiliser l'allocation de mémoire OLE. Pour plus d'informations sur les objets de stockage structuré OLE et l'allocation de mémoire OLE, consultez la rubrique [OLE and Data Transfer](https://msdn.microsoft.com/library/d4a57956-37ba-44ca-8efc-bf617ad5e77b.aspx). 
  

