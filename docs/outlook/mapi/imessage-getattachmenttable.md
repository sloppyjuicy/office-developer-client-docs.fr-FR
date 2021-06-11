---
title: IMessageGetAttachmentTable
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IMessage.GetAttachmentTable
api_type:
- COM
ms.assetid: e568917e-6085-4094-8728-89ba90a78c40
description: 'Derniére modification : samedi 23 juillet 2011'
ms.openlocfilehash: 9a77d335f3c8980de29dab6e14079c83bd711b43
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33421171"
---
# <a name="imessagegetattachmenttable"></a>IMessage::GetAttachmentTable

  
  
**S’applique à** : Outlook 2013 | Outlook 2016 
  
Renvoie la table des pièces jointes du message.
  
```cpp
HRESULT GetAttachmentTable(
  ULONG ulFlags,
  LPMAPITABLE FAR * lppTable
);
```

## <a name="parameters"></a>Parameters

 _ulFlags_
  
> [in] Masque de bits d’indicateurs liés à la création de la table. L’indicateur suivant peut être définie : 
    
MAPI_UNICODE 
  
> Les colonnes de chaîne sont au format Unicode. Si l’MAPI_UNICODE n’est pas définie, les colonnes de chaîne sont au format ANSI.
    
MAPI_DEFERRED_ERRORS 
  
> Permet à **GetAttachmentTable** de renvoyer correctement, éventuellement avant que la table soit entièrement disponible pour le client appelant. Si la table n’est pas disponible, un appel ultérieur à celui-ci peut provoquer une erreur. 
    
 _lppTable_
  
> [out] Pointeur vers un pointeur vers le tableau des pièces jointes.
    
## <a name="return-value"></a>Valeur renvoyée

S_OK 
  
> La table des pièces jointes a été récupérée avec succès.
    
## <a name="remarks"></a>Remarques

La **méthode IMessage::GetAttachmentTable** renvoie un pointeur vers la table des pièces jointes du message, qui inclut des informations sur toutes les pièces jointes du message. Les clients peuvent accéder à une pièce jointe uniquement par le biais de la table des pièces jointes. En récupérant le numéro d’une pièce jointe, sa propriété **PR_ATTACH_NUM** ([PidTagAttachNumber](pidtagattachnumber-canonical-property.md)) permet à un client d’utiliser plusieurs méthodes **IMessage** pour travailler avec la pièce jointe. 
  
Il existe une ligne pour chaque pièce jointe. Pour obtenir la liste complète des colonnes d’une table de pièces jointes, voir [Tables des pièces jointes.](attachment-tables.md)
  
Une pièce jointe n’apparaît généralement pas dans la table des pièces jointes tant que la pièce jointe et le message n’ont pas été enregistrés avec un appel [à IMAPIProp::SaveChanges](imapiprop-savechanges.md). Les tables de pièces jointes sont dynamiques. Si un client crée une pièce jointe, supprime une pièce jointe existante ou modifie une ou plusieurs propriétés une fois que les appels **SaveChanges** ont été effectués sur la pièce jointe du message, la table des pièces jointes est mise à jour pour refléter les nouvelles informations. 
  
Certaines tables de pièces jointes supportent un large éventail de restrictions . d’autres non. La prise en charge des restrictions dépend de l’implémentation du fournisseur de magasins de messages. 
  
Lors de l’ouverture initiale, les tables de pièces jointes ne sont pas nécessairement triées dans un ordre particulier. 
  
La définition MAPI_UNICODE’indicateur dans le  _paramètre ulFlags_ affecte les appels suivants à la table des pièces jointes : 
  
- [IMAPITable::QueryColumns](imapitable-querycolumns.md) pour récupérer le jeu de colonnes. 
    
- [IMAPITable::QueryRows](imapitable-queryrows.md) pour récupérer des lignes. 
    
- [IMAPITable::QuerySortOrder](imapitable-querysortorder.md) pour récupérer l’ordre de tri. 
    
La définition de l’indicateur Unicode demande que les informations des colonnes de chaîne renvoyées par ces appels soient au format Unicode. Toutefois, étant donné que tous les fournisseurs de banque de messages ne sont pas en charge Unicode, la définition de cet indicateur n’est qu’une demande.
  
## <a name="see-also"></a>Voir aussi



[IMessage::CreateAttach](imessage-createattach.md)
  
[IMessage::DeleteAttach](imessage-deleteattach.md)
  
[IMessage::OpenAttach](imessage-openattach.md)
  
[IMessage : IMAPIProp](imessageimapiprop.md)

