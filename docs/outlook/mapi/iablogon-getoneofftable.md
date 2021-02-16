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
description: 'Derniére modification : samedi 23 juillet 2011'
ms.openlocfilehash: 326a78ed512ec82a9f16b1540aad60954ab2d864
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33411875"
---
# <a name="iablogongetoneofftable"></a>IABLogon::GetOneOffTable

  
  
**S’applique à** : Outlook 2013 | Outlook 2016 
  
Renvoie une table de modèles unique pour la création de destinataires à ajouter à la liste des destinataires d’un message sortant.
  
```cpp
HRESULT GetOneOffTable(
  ULONG ulFlags,
  LPMAPITABLE FAR * lppTable
);
```

## <a name="parameters"></a>Paramètres

 _ulFlags_
  
> [in] Masque de bits d’indicateurs qui contrôle le type de colonnes de chaîne incluses dans le tableau. L’indicateur suivant peut être définie :
    
MAPI_UNICODE 
  
> Les colonnes de chaîne sont au format Unicode. Si l’MAPI_UNICODE n’est pas définie, les colonnes de chaîne sont au format ANSI.
    
 _lppTable_
  
> [out] Pointeur vers un pointeur vers le tableau one-off.
    
## <a name="return-value"></a>Valeur renvoyée

S_OK 
  
> La table a été récupérée avec succès.
    
MAPI_E_BAD_CHARWIDTH 
  
> L’indicateur MAPI_UNICODE a été définie et le fournisseur de carnet d’adresses ne prend pas en charge Unicode, ou MAPI_UNICODE n’a pas été définie et le fournisseur de carnet d’adresses prend uniquement en charge Unicode.
    
MAPI_E_NO_SUPPORT 
  
> Le fournisseur de carnet d’adresses ne fournit aucun modèle unique.
    
## <a name="remarks"></a>Remarques

MAPI appelle la **méthode GetOneOffTable** pour mettre à disposition des modèles one-off pour créer des destinataires. Les nouveaux destinataires sont ajoutés à la liste des destinataires d’un message sortant. Les fournisseurs de carnets d’adresses doivent prendre en charge les notifications sur leur tableau unique pour informer MAPI des modifications apportées aux modèles. MAPI maintient la table ouverte pour activer la mise à jour dynamique. 
  
Les fournisseurs de carnets d’adresses peuvent également prendre en charge une table one-off pour chacun de leurs conteneurs. Les appelants récupèrent cette table en appelant la méthode [IMAPIProp::OpenProperty](imapiprop-openproperty.md) du conteneur et en demandant la propriété **PR_CREATE_TEMPLATES** ([PidTagCreateTemplates](pidtagcreatetemplates-canonical-property.md)). Les modèles disponibles dans ce tableau sont utilisés pour ajouter des destinataires au conteneur. Pour obtenir une discussion sur les différences entre les deux types de tableaux one-off, voir [Implementing One-Off Tables](implementing-one-off-tables.md).
  
Pour obtenir la liste des colonnes requises dans la table un-off d’un fournisseur de carnet d’adresses, voir [Tables one-off.](one-off-tables.md)
  
## <a name="see-also"></a>Voir aussi



[IABContainer::CreateEntry](iabcontainer-createentry.md)
  
[IAddrBook::NewEntry](iaddrbook-newentry.md)
  
[IMAPISupport::GetOneOffTable](imapisupport-getoneofftable.md)
  
[IABLogon : IUnknown](iablogoniunknown.md)

