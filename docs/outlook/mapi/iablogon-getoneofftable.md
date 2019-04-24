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
description: 'Dernière modification : 23 juillet 2011'
ms.openlocfilehash: 326a78ed512ec82a9f16b1540aad60954ab2d864
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32338408"
---
# <a name="iablogongetoneofftable"></a>IABLogon::GetOneOffTable

  
  
**S’applique à** : Outlook 2013 | Outlook 2016 
  
Renvoie une table des modèles uniques permettant de créer des destinataires à ajouter à la liste des destinataires d'un message sortant.
  
```cpp
HRESULT GetOneOffTable(
  ULONG ulFlags,
  LPMAPITABLE FAR * lppTable
);
```

## <a name="parameters"></a>Paramètres

 _ulFlags_
  
> dans Masque de des indicateurs qui contrôle le type de colonnes de chaîne incluses dans le tableau. L'indicateur suivant peut être défini:
    
MAPI_UNICODE 
  
> Les colonnes de chaîne sont au format Unicode. Si l'indicateur MAPI_UNICODE n'est pas défini, les colonnes de la chaîne sont au format ANSI.
    
 _lppTable_
  
> remarquer Pointeur vers un pointeur vers la table ponctuelle.
    
## <a name="return-value"></a>Valeur renvoyée

S_OK 
  
> La table ponctuelle a été récupérée avec succès.
    
MAPI_E_BAD_CHARWIDTH 
  
> L'indicateur MAPI_UNICODE a été défini et le fournisseur de carnet d'adresses ne prend pas en charge Unicode, ou MAPI_UNICODE n'a pas été défini et le fournisseur de carnet d'adresses prend en charge uniquement Unicode.
    
MAPI_E_NO_SUPPORT 
  
> Le fournisseur de carnet d'adresses ne fournit pas de modèles uniques.
    
## <a name="remarks"></a>Remarques

MAPI appelle la méthode **GetOneOffTable** pour mettre à disposition des modèles uniques pour créer des destinataires. Les nouveaux destinataires sont ajoutés à la liste des destinataires d'un message sortant. Les fournisseurs de carnets d'adresses doivent prendre en charge la notification sur leur table ponctuelle pour informer MAPI des modifications de modèle. MAPI conserve la table ponctuelle ouverte pour activer la mise à jour dynamique. 
  
Les fournisseurs de carnets d'adresses peuvent également prendre en charge une table ponctuelle pour chacun de leurs conteneurs. Les appelants extraient cette table ponctuelle en appelant la méthode [IMAPIProp:: OpenProperty](imapiprop-openproperty.md) du conteneur et en demandant la propriété **PR_CREATE_TEMPLATES** ([PidTagCreateTemplates](pidtagcreatetemplates-canonical-property.md)). Les modèles disponibles dans ce tableau permettent d'ajouter des destinataires au conteneur. Pour plus d'informations sur les différences entre les deux types de tables ponctuelles, reportez-vous à la rubrique [implementIng One-Off tables](implementing-one-off-tables.md).
  
Pour obtenir la liste des colonnes requises dans la table ponctuelle d'un fournisseur de carnet d'adresses, consultez la rubrique [tables One-Off](one-off-tables.md).
  
## <a name="see-also"></a>Voir aussi



[IABContainer::CreateEntry](iabcontainer-createentry.md)
  
[IAddrBook::NewEntry](iaddrbook-newentry.md)
  
[IMAPISupport::GetOneOffTable](imapisupport-getoneofftable.md)
  
[IABLogon : IUnknown](iablogoniunknown.md)

