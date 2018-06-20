---
title: ITnefEncodeRecips
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- ITnef.EncodeRecips
api_type:
- COM
ms.assetid: b3ce4b0e-4f48-4a7e-a30c-c4754bccb12c
description: 'Derni�re modification�: samedi 23 juillet 2011'
ms.openlocfilehash: edabb9a0f55cb34b4e144672e91ea50b8e9193b0
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19784474"
---
# <a name="itnefencoderecips"></a>ITnef::EncodeRecips

  
  
**S’applique à**: Outlook 
  
Encode un affichage pour la table des destinataires d’un message dans le flux de données de Transport-Neutral Encapsulation Format (TNEF) pour le message.
  
```cpp
HRESULT EncodeRecips(
  ULONG ulFlags,
  LPMAPITABLE lpRecipientTable
);
```

## <a name="parameters"></a>Param�tres

 _ulFlags_
  
> [in] R�serv� ; doit �tre �gal � z�ro.
    
 _lpRecipientTable_
  
> [in] Pointeur vers la table de destinataires pour lesquels l’affichage est codé. Le paramètre _lpRecipientTable_ peut être NULL. 
    
## <a name="return-value"></a>Valeur renvoy�e

S_OK 
  
> L’appel a réussi et renvoyé la valeur attendue ou les valeurs.
    
## <a name="remarks"></a>Remarques

Transport, fournisseurs de banque de message et passerelles appel la méthode **ITnef::EncodeRecips** pour effectuer le codage TNEF pour un affichage tableau destinataire particulier. Le codage TNEF est utile, par exemple, si un fournisseur ou une passerelle nécessite un ensemble de colonnes particulier, ordre de tri ou restriction pour la table de destinataires. 
  
Un fournisseur ou une passerelle transmet l’affichage tableau doivent être codées dans le paramètre _lpRecipientTable_ . L’implémentation TNEF encode la table de destinataires avec la vue spécifiée, à l’aide de la colonne donnée set, ordre de tri, les restrictions et position. Si un fournisseur ou une passerelle passe NULL _lpRecipientTable_, TNEF Obtient la table de destinataires du message encodé à l’aide de la méthode [IMessage::GetRecipientTable](imessage-getrecipienttable.md) , processus et chaque ligne du tableau dans le flux TNEF à l’aide de la paramètres actuels de la table. 
  
Appel **EncodeRecips** avec la valeur NULL dans _lpRecipientTable_ ainsi encode tous les destinataires du message et revient à appeler la méthode [ITnef::AddProps](itnef-addprops.md) avec l’indicateur TNEF_PROP_INCLUDE dans son paramètre _ulFlags_ et la **PR_ MESSAGE_RECIPIENTS** ([PidTagMessageRecipients](pidtagmessagerecipients-canonical-property.md)) propriété dans son paramètre _lpPropList_ . 
  
Notez qu’il est rarement nécessaire d’appeler **EncodeRecips** sauf s’il existe une condition requise pour coder un affichage de tableau destinataire particulier. Systèmes de messagerie étrangers ont presque toujours des outils de gestion des listes de destinataires qui sont suffisamment puissants pour gérer les besoins courants de codage des listes de destinataires ; Par conséquent, ces systèmes nécessitent pratiquement jamais TNEF à cet effet. 
  
## <a name="see-also"></a>Voir aussi



[IMessage::GetRecipientTable](imessage-getrecipienttable.md)
  
[ITnef::AddProps](itnef-addprops.md)
  
[Propriété canonique PidTagMessageRecipients](pidtagmessagerecipients-canonical-property.md)
  
[ITnef : IUnknown](itnefiunknown.md)

