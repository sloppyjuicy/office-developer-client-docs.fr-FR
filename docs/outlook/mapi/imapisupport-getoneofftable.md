---
title: IMAPISupportGetOneOffTable
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
api_name:
- IMAPISupport.GetOneOffTable
api_type:
- COM
ms.assetid: 6800fd3a-aa43-45fe-9cc2-102d0ef43edf
description: 'Derniére modification : samedi 23 juillet 2011'
ms.openlocfilehash: 55958af9d68ac27a92f06528dbc8fbc1fc62e574
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/24/2021
ms.locfileid: "59556510"
---
# <a name="imapisupportgetoneofftable"></a>IMAPISupport::GetOneOffTable

  
  
**S’applique à** : Outlook 2013 | Outlook 2016 
  
Renvoie un pointeur vers le tableau unique MAPI (liste de modèles que tous les fournisseurs de carnet d’adresses peuvent prendre en charge pour la création de destinataires).
  
```cpp
HRESULT GetOneOffTable(
  ULONG ulFlags,
  LPMAPITABLE FAR * lppTable
);
```

## <a name="parameters"></a>Paramètres

 _ulFlags_
  
> [in] Masque de bits d’indicateurs qui contrôle le type des colonnes de chaîne. L’indicateur suivant peut être définie :
    
MAPI_UNICODE 
  
> Les colonnes de chaîne sont au format Unicode. Si l’MAPI_UNICODE n’est pas définie, les colonnes de chaîne sont au format ANSI.
    
 _lppTable_
  
> [out] Pointeur vers un pointeur vers le tableau one-off.
    
## <a name="return-value"></a>Valeur renvoyée

S_OK 
  
> La table a été récupérée avec succès.
    
## <a name="remarks"></a>Remarques

La **méthode IMAPISupport::GetOneOffTable** est implémentée pour les objets de prise en charge du fournisseur de carnet d’adresses. Les fournisseurs de carnet d’adresses **appellent GetOneOffTable** pour récupérer la liste complète des modèles de création de destinataires. Ce tableau inclut des modèles qui sont des fournisseurs de carnet d’adresses qui sont actifs dans la prise en charge de session, ainsi que des modèles que MAPI prend en charge. 
  
Les destinataires nouvellement créés peuvent être utilisés pour adresser un message ou peuvent être ajoutés à un conteneur de carnet d’adresses.
  
Pour obtenir la liste des propriétés qui font partie de la colonne requise définie dans des tables uniques, voir [Tables uniques.](one-off-tables.md)
  
La définition de l’indicateur MAPI_UNICODE dans le paramètre _ulFlags_ affecte le format des colonnes renvoyées par les méthodes [IMAPITable::QueryColumns](imapitable-querycolumns.md) et [IMAPITable::QueryRows.](imapitable-queryrows.md) Cet indicateur contrôle également les types de propriétés dans l’ordre de tri renvoyé par la méthode [IMAPITable::QuerySortOrder.](imapitable-querysortorder.md) 
  
## <a name="notes-to-callers"></a>Remarques pour les appelants

Si vous êtes inscrit pour recevoir des notifications de modifications apportées à ce tableau one-off, vous recevrez également des notifications de modifications apportées aux tables one-off d’autres fournisseurs. En fonction de ces notifications, vous pouvez prendre en charge les nouveaux types d’adresses ajoutés au cours de la session en cours.
  
## <a name="see-also"></a>Voir aussi



[IABContainer::CreateEntry](iabcontainer-createentry.md)
  
[IMAPISupport::NewEntry](imapisupport-newentry.md)
  
[IMAPITable : IUnknown](imapitableiunknown.md)
  
[IMAPITable::QueryColumns](imapitable-querycolumns.md)
  
[IMAPITable::QueryRows](imapitable-queryrows.md)
  
[IMAPITable::QuerySortOrder](imapitable-querysortorder.md)
  
[Propriété canonique PidTagCreateTemplates](pidtagcreatetemplates-canonical-property.md)
  
[IMAPISupport : IUnknown](imapisupportiunknown.md)


[One-Off Tables](one-off-tables.md)

