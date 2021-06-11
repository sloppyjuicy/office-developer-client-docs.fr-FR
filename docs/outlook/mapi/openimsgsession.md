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
description: Dernière modification le 9 mars 2015
ms.openlocfilehash: 607105bd58a14a3510f1ae71246069440a4f05cb
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32326193"
---
# <a name="openimsgsession"></a>OpenIMsgSession

  
  
**S’applique à** : Outlook 2013 | Outlook 2016 
  
Crée et ouvre une session de message qui groupe les messages créés au sein de celle-ci. 
  
|||
|:-----|:-----|
|Fichier d’en-tête :  <br/> |Imessage.h  <br/> |
|Implémenté par :  <br/> |MAPI  <br/> |
|Appelé par :  <br/> |Applications clientes et fournisseurs de services  <br/> |
   
```cpp
SCODE OpenIMsgSession(
  LPMALLOC lpMalloc,
  ULONG ulFlags,
  LPMSGSESS FAR * lppMsgSess
);
```

## <a name="parameters"></a>Parameters

 _lpMalloc_
  
> [in] Pointeur vers un objet d’allocation de mémoire exposant l’interface OLE [IMalloc.](https://docs.microsoft.com/windows/desktop/api/objidl/nn-objidl-imalloc) MAPI doit utiliser cette méthode d’allocation lors de l’utilisation de l’interface OLE [IStorage.](https://docs.microsoft.com/windows/desktop/api/objidl/nn-objidl-istorage) 
    
 _ulFlags_
  
> [in] R�serv� ; doit �tre �gal � z�ro. 
    
 _lppMsgSess_
  
> [out] Pointeur vers un pointeur vers l’objet de session de message renvoyé.
    
## <a name="return-value"></a>Valeur renvoyée

S_OK
  
> La session a été ouverte.
    
MAPI_E_INVALID_PARAMETER
  
>  _lpMalloc_ ou  _lppMsgSess_ est NULL. 
    
MAPI_E_INVALID_FLAGS
  
> Des indicateurs non valides ont été transmis.
    
MAPI_UNICODE
  
> Lorsque vous appelez cette fonction, un client ou un fournisseur de services définit l’MAPI_UNICODE pour créer des fichiers .msg Unicode. Le fichier [Imessage](imessageimapiprop.md) qui en résulte affiche les STORE_UNICODE_OK sa PR_STORE_SUPPORT_MASK et prend en charge les propriétés Unicode. 
    
## <a name="remarks"></a>Remarques

Une session de message est utilisée par les applications clientes et les fournisseurs de services qui souhaitent traiter plusieurs objets [MAPI IMessage : IMAPIProp](imessageimapiprop.md) créés au-dessus des objets OLE **IStorage** sous-jacents. Le client ou le fournisseur utilise les fonctions **OpenIMsgSession** et [CloseIMsgSession](closeimsgsession.md) pour encapsuler la création de tels messages dans une session de message. Une fois la session de message ouverte, le client ou le fournisseur lui transmet un pointeur dans un appel à [OpenIMsgOnIStg](openimsgonistg.md) pour créer un objet **IMessage**-on- **IStorage.** 
  
Une session de message assure le suivi de tous les objets **IMessage**-on- **IStorage** créés pendant la durée de la session, en plus de toutes les pièces jointes et autres propriétés des messages. Lorsqu’un client ou un fournisseur appelle **CloseIMsgSession,** il ferme tous ces objets. L’appel de **CloseIMsgSession** est le seul moyen de fermer des objets **IMessage**-on- **IStorage.** 
  
 **OpenIMsgSession** est utilisé par les clients et les fournisseurs qui nécessitent la possibilité de gérer plusieurs messages associés en tant qu’objets **OLE IStorage.** Si un seul de ces messages doit être ouvert à la fois, il n’est pas nécessaire de suivre plusieurs messages et il n’y a aucune raison de créer une session de message avec **OpenIMsgSession**. 
  
Étant donné qu’il traite un objet OLE sous-jacent, MAPI doit utiliser l’allocation de mémoire OLE. Pour plus d’informations sur les objets de stockage structuré OLE et l’allocation de mémoire OLE, voir [OLE et Transfert de données.](https://msdn.microsoft.com/library/d4a57956-37ba-44ca-8efc-bf617ad5e77b.aspx) 
  

