---
title: OpenIMsgSession
description: Décrit la syntaxe, les paramètres et la valeur de retour d’OpenIMsgSession, qui crée et ouvre une session de messages qui regroupe les messages créés dans celle-ci.
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
api_name:
- MAPI.OpenIMsgSession
api_type:
- COM
ms.assetid: f75229e3-5f44-4298-8706-9eddf0ef124c
ms.openlocfilehash: d1a6739c85804b9c0a7be2a372a541b618985a62
ms.sourcegitcommit: 1b44c8f9eac3aedaf7fe7ec70c808fe8ed7d4b99
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/02/2022
ms.locfileid: "65854727"
---
# <a name="openimsgsession"></a>OpenIMsgSession

**S’applique à** : Outlook 2013 | Outlook 2016
  
Crée et ouvre une session de messages qui regroupe les messages qu’elle contient.
  
|Propriété |Valeur |
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

## <a name="parameters"></a>Paramètres

 _lpMalloc_

> [in] Pointeur vers un objet allocateur de mémoire exposant l’interface OLE [IMalloc](/windows/desktop/api/objidl/nn-objidl-imalloc) . MAPI doit utiliser cette méthode d’allocation lors de l’utilisation de l’interface OLE [IStorage](/windows/desktop/api/objidl/nn-objidl-istorage) .

 _ulFlags_

> [in] R�serv� ; doit �tre �gal � z�ro.

 _lppMsgSess_

> [out] Pointeur vers un pointeur vers l’objet de session de message retourné.

## <a name="return-value"></a>Valeur renvoyée

S_OK

> La session a été ouverte.

MAPI_E_INVALID_PARAMETER

> _lpMalloc_ ou _lppMsgSess_ a la valeur NULL.

MAPI_E_INVALID_FLAGS

> Des indicateurs non valides ont été passés.

MAPI_UNICODE

> Lors de l’appel de cette fonction, un client ou un fournisseur de services définit l’indicateur MAPI_UNICODE pour créer des fichiers .msg Unicode. Le fichier [Imessage](imessageimapiprop.md) résultant affiche STORE_UNICODE_OK dans son PR_STORE_SUPPORT_MASK et prend en charge les propriétés Unicode.

## <a name="remarks"></a>Remarques

Une session de message est utilisée par les applications clientes et les fournisseurs de services qui souhaitent traiter plusieurs objets [MAPI IMessage : IMAPIProp](imessageimapiprop.md) associés basés sur des objets OLE **IStorage sous-jacents** . Le client ou le fournisseur utilise les fonctions **OpenIMsgSession** et [CloseIMsgSession](closeimsgsession.md) pour encapsuler la création de ces messages dans une session de message. Une fois la session de message ouverte, le client ou le fournisseur lui transmet un pointeur dans un appel à [OpenIMsgOnIStg](openimsgonistg.md) pour créer un objet IMessage-on-IStorage.

Une session de message effectue le suivi de tous les objets **IMessage-on-IStorage créés** pendant la durée de la session, en plus de toutes les pièces jointes et autres propriétés des messages. Lorsqu’un client ou un fournisseur appelle **CloseIMsgSession**, il ferme tous ces objets. L’appel de **CloseIMsgSession** est la seule façon de fermer des objets IMessage-on-IStorage.

 **OpenIMsgSession** est utilisé par les clients et les fournisseurs qui nécessitent la possibilité de gérer plusieurs messages associés en tant qu’objets OLE **IStorage** . Si un seul de ces messages doit être ouvert à la fois, il n’est pas nécessaire de suivre plusieurs messages et aucune raison de créer une session de message avec **OpenIMsgSession**.

Étant donné qu’il traite d’un objet OLE sous-jacent, MAPI doit utiliser l’allocation de mémoire OLE. Pour plus d’informations sur les objets de stockage structuré OLE et l’allocation de mémoire OLE, consultez [OLE et Transfert de données](https://msdn.microsoft.com/library/d4a57956-37ba-44ca-8efc-bf617ad5e77b.aspx).
 