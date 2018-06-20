---
title: IABLogonGetOneOffTable
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IABLogon.GetOneOffTable
api_type:
- COM
ms.assetid: 7ac2a8d4-6890-4346-a6b6-34deca9dab50
description: 'Derni�re modification�: samedi 23 juillet 2011'
ms.openlocfilehash: b8a6d74df3749a5445d95ad392f7f88d27190bfc
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19783591"
---
# <a name="iablogongetoneofftable"></a>IABLogon::GetOneOffTable

  
  
**S’applique à**: Outlook 
  
Renvoie un tableau des modèles uniques pour la création de destinataires à ajouter à la liste des destinataires d’un message sortant.
  
```cpp
HRESULT GetOneOffTable(
  ULONG ulFlags,
  LPMAPITABLE FAR * lppTable
);
```

## <a name="parameters"></a>Param�tres

 _ulFlags_
  
> [in] Masque de bits d’indicateurs qui contrôle le type des colonnes de chaîne inclus dans le tableau. Vous pouvez définir l’indicateur suivant :
    
MAPI_UNICODE 
  
> Les colonnes de type chaîne sont au format Unicode. Si l’indicateur MAPI_UNICODE n’est pas définie, les colonnes de type chaîne sont au format ANSI.
    
 _lppTable_
  
> [out] Pointeur vers un pointeur vers la table unique.
    
## <a name="return-value"></a>Valeur renvoy�e

S_OK 
  
> Le tableau unique a été récupéré correctement.
    
MAPI_E_BAD_CHARWIDTH 
  
> Soit l’indicateur MAPI_UNICODE a été défini et le fournisseur de carnet d’adresses ne prend pas en charge Unicode, ou MAPI_UNICODE n’a pas été définie et le fournisseur de carnet d’adresses prend en charge Unicode uniquement.
    
MAPI_E_NO_SUPPORT 
  
> Le fournisseur de carnet d’adresses ne fournit pas de modèles uniques.
    
## <a name="remarks"></a>Remarques

MAPI appelle la méthode **GetOneOffTable** pour rendre des modèles uniques disponibles pour créer des destinataires. Les nouveaux destinataires sont ajoutés à la liste des destinataires d’un message sortant. Fournisseurs de carnet d’adresses doivent prendre en charge la notification sur leur table unique pour informer les MAPI de modifications du modèle. MAPI tenir à jour la table unique open pour activer la mise à jour dynamique. 
  
Fournisseurs de carnet d’adresses peuvent également en charge une table unique pour chacune de leurs conteneurs. Les appelants récupérer ce tableau unique à l’appel de méthode [d’IMAPIProp::OpenProperty](imapiprop-openproperty.md) du conteneur et demande la propriété **PR_CREATE_TEMPLATES** ([PidTagCreateTemplates](pidtagcreatetemplates-canonical-property.md)). Les modèles disponibles par le biais de cette table sont utilisés pour ajouter des destinataires dans le conteneur. Pour une description des différences entre les deux types de tables uniques, voir [Implémentation de Tables uniques](implementing-one-off-tables.md).
  
Pour obtenir la liste des colonnes requises dans la table uniques d’un fournisseur de carnet d’adresses, voir [Les Tables uniques](one-off-tables.md).
  
## <a name="see-also"></a>Voir aussi



[IABContainer::CreateEntry](iabcontainer-createentry.md)
  
[IAddrBook::NewEntry](iaddrbook-newentry.md)
  
[IMAPISupport::GetOneOffTable](imapisupport-getoneofftable.md)
  
[IABLogon : IUnknown](iablogoniunknown.md)

