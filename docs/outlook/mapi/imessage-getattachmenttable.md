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
ms.openlocfilehash: bf100ed916080a91366062f45b9e3349516bdb98
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/23/2018
ms.locfileid: "22588516"
---
# <a name="imessagegetattachmenttable"></a>IMessage::GetAttachmentTable

  
  
**S’applique à** : Outlook 2013 | Outlook 2016 
  
Renvoie un tableau de pièce jointe du message.
  
```cpp
HRESULT GetAttachmentTable(
  ULONG ulFlags,
  LPMAPITABLE FAR * lppTable
);
```

## <a name="parameters"></a>Param�tres

 _ulFlags_
  
> [in] Masque de bits d’indicateurs qui sont associées à la création de la table. Vous pouvez définir l’indicateur suivant : 
    
MAPI_UNICODE 
  
> Les colonnes de type chaîne sont au format Unicode. Si l’indicateur MAPI_UNICODE n’est pas définie, les colonnes de type chaîne sont au format ANSI.
    
MAPI_DEFERRED_ERRORS 
  
> Permet de **GetAttachmentTable** renvoyer avec succès, éventuellement, avant de la table est totalement disponible au client appelant. Si le tableau n’est pas disponible, vous appelez suivante lui peut provoquer une erreur. 
    
 _lppTable_
  
> [out] Pointeur vers un pointeur vers la table des pièces jointes.
    
## <a name="return-value"></a>Valeur renvoyée

S_OK 
  
> Le tableau de pièce jointe a été récupéré correctement.
    
## <a name="remarks"></a>Remarques

La méthode **IMessage::GetAttachmentTable** retourne un pointeur vers la table de pièce jointe du message, qui consacrée des informations sur toutes les pièces jointes dans le message. Les clients peuvent accéder à une pièce jointe uniquement par le biais de la table des pièces jointes. En récupérant le numéro d’une pièce jointe sa propriété **PR_ATTACH_NUM** ([PidTagAttachNumber](pidtagattachnumber-canonical-property.md)) un client peut utiliser plusieurs méthodes **IMessage** pour fonctionner avec la pièce jointe. 
  
Il existe une ligne pour chaque pièce jointe. Pour obtenir une liste complète des colonnes dans une table des pièces jointes, voir les [Tables des pièces jointes](attachment-tables.md).
  
Une pièce jointe n’apparaît généralement pas dans la table des pièces jointes jusqu'à ce que la pièce jointe et le message ont été enregistrés avec un appel à [IMAPIProp::SaveChanges](imapiprop-savechanges.md). Tables des pièces jointes sont dynamiques. Si un client crée une pièce jointe, supprime une pièce jointe existante ou modifie une ou plusieurs propriétés une fois que les appels **SaveChanges** ont été apportées sur la pièce jointe du message, la table des pièces jointes système mis à jour pour refléter les nouvelles informations. 
  
Certaines tables des pièces jointes prend en charge une grande variété de restrictions ; d’autres ne le sont pas. Prise en charge des restrictions dépend de l’implémentation du fournisseur de banque de messages. 
  
Ouverture à l’origine, tables des pièces jointes ne sont pas nécessairement triées selon un ordre particulier. 
  
Définition de l’indicateur MAPI_UNICODE dans le paramètre _ulFlags_ affecte les appels suivants de la table des pièces jointes : 
  
- [IMAPITable::QueryColumns](imapitable-querycolumns.md) pour extraire l’ensemble de colonnes. 
    
- [IMAPITable::QueryRows](imapitable-queryrows.md) pour récupérer des lignes. 
    
- [IMAPITable::QuerySortOrder](imapitable-querysortorder.md) pour récupérer l’ordre de tri. 
    
Si les demandes d’indicateur Unicode que les informations des colonnes de la chaîne retournée par ces appels au format Unicode. Toutefois, étant donné que tous les fournisseurs de banque de messages prennent en charge Unicode, définition de cet indicateur est uniquement une demande.
  
## <a name="see-also"></a>Voir aussi



[IMessage::CreateAttach](imessage-createattach.md)
  
[IMessage::DeleteAttach](imessage-deleteattach.md)
  
[IMessage::OpenAttach](imessage-openattach.md)
  
[IMessage : IMAPIProp](imessageimapiprop.md)

