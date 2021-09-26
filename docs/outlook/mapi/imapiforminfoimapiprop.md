---
title: IMAPIFormInfo IMAPIProp
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
api_name:
- IMAPIFormInfo
api_type:
- COM
ms.assetid: a9fda518-11ba-42aa-85ef-dd2279e0319d
description: Dernière modification le 9 mars 2015
ms.openlocfilehash: 65c00ba95a38005b953e704eafa76cf5e2df4e77
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/24/2021
ms.locfileid: "59610586"
---
# <a name="imapiforminfo--imapiprop"></a>IMAPIFormInfo : IMAPIProp

  
  
**S’applique à** : Outlook 2013 | Outlook 2016 
  
Permet aux applications clientes d’accéder aux propriétés qui sont spécifiques à la définition de formulaire. En conservant les informations de formulaire dans un objet distinct, le fournisseur de bibliothèque de formulaires peut décrire un formulaire à un client sans l’activer.
  
|||
|:-----|:-----|
|Fichier d’en-tête :  <br/> |Mapiform.h  <br/> |
|Exposé par :  <br/> |Objets d’informations de formulaire  <br/> |
|Implémenté par :  <br/> |Fournisseurs de bibliothèques de formulaires  <br/> |
|Appelé par :  <br/> |Applications clientes  <br/> |
|Identificateur d’interface :  <br/> |IID_IMAPIFormInfo  <br/> |
|Type de pointeur :  <br/> |LPMAPIFORMINFO  <br/> |
|Modèle de transaction :  <br/> |Non traduit  <br/> |
   
## <a name="vtable-order"></a>Ordre des vtables

|||
|:-----|:-----|
|[CalcFormPropSet](imapiforminfo-calcformpropset.md) <br/> |Renvoie un pointeur vers l’ensemble complet des propriétés qu’un formulaire utilise.  <br/> |
|[CalcVerbSet](imapiforminfo-calcverbset.md) <br/> |Renvoie un pointeur vers l’ensemble complet des verbes qu’un formulaire utilise.  <br/> |
|[MakeIconFromBinary](imapiforminfo-makeiconfrombinary.md) <br/> |Crée une icône à partir d’une propriété d’icône d’un formulaire.  <br/> |
|[SaveForm](imapiforminfo-saveform.md) <br/> |Enregistre une description d’un formulaire particulier dans un fichier de configuration.  <br/> |
|[OpenFormContainer](imapiforminfo-openformcontainer.md) <br/> |Renvoie un pointeur vers le conteneur de formulaire dans lequel un formulaire particulier est installé.  <br/> |
   
## <a name="remarks"></a>Remarques

Contrairement à la plupart des interfaces définies dans le fichier d’en-tête MapiForm.h, **IMAPIFormInfo** hérite de l’interface [IMAPIProp,](imapipropiunknown.md) car il exporte la plupart des informations de formulaire par le biais d’appels à la méthode [IMAPIProp::GetProps.](imapiprop-getprops.md) 
  
## <a name="see-also"></a>Voir aussi



[Interfaces MAPI](mapi-interfaces.md)

