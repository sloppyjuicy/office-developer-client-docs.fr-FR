---
title: CloseIMsgSession
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.CloseIMsgSession
api_type:
- COM
ms.assetid: a0a17309-fc59-4822-be9b-b6f623b68bb1
description: Dernière modification le 09 mars 2015
ms.openlocfilehash: f358467d72f2a9f395762f529244041a5d9d8d6a
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/23/2018
ms.locfileid: "22575979"
---
# <a name="closeimsgsession"></a>CloseIMsgSession

  
  
**S’applique à**: Outlook 2013 | Outlook 2016 
  
Ferme une session de messagerie et de tous les messages créés dans cette session. 
  
|||
|:-----|:-----|
|Fichier d’en-tête :  <br/> |IMessage.h  <br/> |
|Implémentée par :  <br/> |MAPI  <br/> |
|Appelée par :  <br/> |Les applications clientes et des fournisseurs de services  <br/> |
   
```cpp
VOID CloseIMsgSession(
  LPMSGSESS lpMsgSess
);
```

## <a name="parameters"></a>Paramètres

 _lpMsgSess_
  
> [in] Pointeur vers l’objet de la session message obtenue à l’aide de la fonction [OpenIMsgSession](openimsgsession.md) au début de la session de messagerie. 
    
## <a name="return-value"></a>Valeur renvoyée

Aucun.
  
## <a name="remarks"></a>Remarques

Une session de messagerie est utilisée par les applications clientes et des fournisseurs de services want gérer plusieurs objets MAPI **IMessage** connexes greffées sur des objets OLE **IStorage** sous-jacents. Le client ou le fournisseur utilise les fonctions [OpenIMsgSession](openimsgsession.md) et **CloseIMsgSession** pour encapsuler la création de ces messages à l’intérieur d’une session de messagerie. Une fois la session de messagerie est ouvert, le client ou le fournisseur lui passe un pointeur dans un appel à [OpenIMsgOnIStg](openimsgonistg.md) pour créer un nouveau **IMessage**- sur - objet **IStorage** . 
  
Enregistre une session de messagerie de tous les objets **IMessage**- sur - **IStorage** ouverts pendant la durée de la session, en plus de toutes les pièces jointes et d’autres propriétés des messages. Lorsqu’un client ou un fournisseur appelle **CloseIMsgSession**, il ferme tous ces objets. L’appel de **CloseIMsgSession** est la seule façon de fermer **IMessage**- sur - objets **IStorage** . 
  

