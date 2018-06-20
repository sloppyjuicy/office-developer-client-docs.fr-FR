---
title: IMAPISupportGetOneOffTable
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IMAPISupport.GetOneOffTable
api_type:
- COM
ms.assetid: 6800fd3a-aa43-45fe-9cc2-102d0ef43edf
description: 'Derni�re modification�: samedi 23 juillet 2011'
ms.openlocfilehash: 51cd838164e3de28ab33d6ab8a08a021360f3183
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19783983"
---
# <a name="imapisupportgetoneofftable"></a>IMAPISupport::GetOneOffTable

  
  
**S’applique à**: Outlook 
  
Retourne un pointeur vers le tableau unique de MAPI (une liste des modèles que tous les du carnet d’adresses fournisseurs de prise en charge pour la création de nouveaux destinataires).
  
```cpp
HRESULT GetOneOffTable(
  ULONG ulFlags,
  LPMAPITABLE FAR * lppTable
);
```

## <a name="parameters"></a>Param�tres

 _ulFlags_
  
> [in] Masque de bits d’indicateurs qui contrôle le type des colonnes de chaîne. Vous pouvez définir l’indicateur suivant :
    
MAPI_UNICODE 
  
> Les colonnes de type chaîne sont au format Unicode. Si l’indicateur MAPI_UNICODE n’est pas définie, les colonnes de type chaîne sont au format ANSI.
    
 _lppTable_
  
> [out] Pointeur vers un pointeur vers la table unique.
    
## <a name="return-value"></a>Valeur renvoy�e

S_OK 
  
> Le tableau unique a été récupéré correctement.
    
## <a name="remarks"></a>Remarques

La méthode **IMAPISupport::GetOneOffTable** est implémentée pour les objets de prise en charge du fournisseur adresse téléchargeable. Fournisseurs de carnet d’adresses appellent **GetOneOffTable** pour récupérer la liste complète des modèles pour la création de nouveaux destinataires. Ce tableau inclut les modèles qui prennent en charge des fournisseurs de carnet d’adresses qui sont actifs dans la session, ainsi que des modèles prenant en charge MAPI. 
  
Les destinataires nouvellement créés peuvent être utilisés pour adresser un message ou peuvent être ajoutés à un conteneur de carnet d’adresses.
  
Pour obtenir la liste des propriétés qui composent la colonne requise définie dans les tableaux uniques, voir [Tables uniques](one-off-tables.md).
  
Définition de l’indicateur MAPI_UNICODE dans le paramètre _ulFlags_ affecte le format des colonnes retournées par les méthodes [IMAPITable::QueryColumns](imapitable-querycolumns.md) et [IMAPITable::QueryRows](imapitable-queryrows.md) . Cet indicateur contrôle également les types de propriétés dans l’ordre de tri renvoyé par la méthode [IMAPITable::QuerySortOrder](imapitable-querysortorder.md) . 
  
## <a name="notes-to-callers"></a>Notes aux appelants

Si vous êtes inscrit pour recevoir les notifications des modifications apportées à cette table unique, vous recevrez les notifications des modifications apportées aux tables uniques des autres fournisseurs. En fonction de ces notifications, vous pouvez bénéficier de nouveaux types d’adresses qui sont ajoutés lors de la session en cours.
  
## <a name="see-also"></a>Voir aussi



[IABContainer::CreateEntry](iabcontainer-createentry.md)
  
[IMAPISupport::NewEntry](imapisupport-newentry.md)
  
[IMAPITable : IUnknown](imapitableiunknown.md)
  
[IMAPITable::QueryColumns](imapitable-querycolumns.md)
  
[IMAPITable::QueryRows](imapitable-queryrows.md)
  
[IMAPITable::QuerySortOrder](imapitable-querysortorder.md)
  
[Propriété canonique PidTagCreateTemplates](pidtagcreatetemplates-canonical-property.md)
  
[IMAPISupport : IUnknown](imapisupportiunknown.md)


[Tables uniques](one-off-tables.md)

