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
description: Donne aux applications clientes l’accès aux propriétés qui sont spécifiques à la définition de formulaire. Le fournisseur peut décrire un formulaire sans l’activer.
ms.openlocfilehash: 4a6e36df62d660fa2abd9b253d38afd24de8d94e
ms.sourcegitcommit: 138c9e15adc07c6ecd740257872aaee6a1a1a7fd
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/25/2022
ms.locfileid: "64406406"
---
# <a name="imapiforminfo--imapiprop"></a>IMAPIFormInfo : IMAPIProp

  
  
**S’applique à** : Outlook 2013 | Outlook 2016 
  
Donne aux applications clientes l’accès aux propriétés qui sont spécifiques à la définition de formulaire. En conservant les informations de formulaire dans un objet distinct, le fournisseur de bibliothèque de formulaires peut décrire un formulaire à un client sans l’activer.
  
|Propriété |Valeur |
|:-----|:-----|
|Fichier d’en-tête :  <br/> |Mapiform.h  <br/> |
|Exposé par :  <br/> |Objets d’informations de formulaire  <br/> |
|Implémenté par :  <br/> |Fournisseurs de bibliothèques de formulaires  <br/> |
|Appelé par :  <br/> |Applications clientes  <br/> |
|Identificateur d’interface :  <br/> |IID_IMAPIFormInfo  <br/> |
|Type de pointeur :  <br/> |LPMAPIFORMINFO  <br/> |
|Modèle de transaction :  <br/> |Non traduit  <br/> |
   
## <a name="vtable-order"></a>Ordre des vtables

|Member |Description |
|:-----|:-----|
|[CalcFormPropSet](imapiforminfo-calcformpropset.md) <br/> |Renvoie un pointeur vers l’ensemble complet des propriétés qu’un formulaire utilise. |
|[CalcVerbSet](imapiforminfo-calcverbset.md) <br/> |Renvoie un pointeur vers l’ensemble complet des verbes qu’un formulaire utilise. |
|[MakeIconFromBinary](imapiforminfo-makeiconfrombinary.md) <br/> |Crée une icône à partir d’une propriété d’icône d’un formulaire. |
|[SaveForm](imapiforminfo-saveform.md) <br/> |Enregistre une description d’un formulaire particulier dans un fichier de configuration. |
|[OpenFormContainer](imapiforminfo-openformcontainer.md) <br/> |Renvoie un pointeur vers le conteneur de formulaire dans lequel un formulaire particulier est installé. |
   
## <a name="remarks"></a>Remarques

Contrairement à la plupart des interfaces définies dans le fichier d’en-tête MapiForm.h, **IMAPIFormInfo** hérite de l’interface [IMAPIProp](imapipropiunknown.md) , car il exporte la plupart des informations de formulaire par le biais d’appels à la méthode [IMAPIProp::GetProps](imapiprop-getprops.md) . 
  
## <a name="see-also"></a>Voir aussi



[Interfaces MAPI](mapi-interfaces.md)

