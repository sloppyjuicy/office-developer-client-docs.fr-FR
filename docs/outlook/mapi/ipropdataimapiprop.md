---
title: IPropData IMAPIProp
description: IPropData IMAPIProp permet de récupérer et de modifier l’accès aux propriétés d’un objet.
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
api_name:
- IPropData
api_type:
- COM
ms.assetid: 30b8ae9e-0c0c-4468-b286-29e083696fed
ms.openlocfilehash: 91716de6720210debaff5b7447f15490529d3803
ms.sourcegitcommit: e2b79cc4469013a4b3705620a93aa70b88e6c996
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/02/2022
ms.locfileid: "65828128"
---
# <a name="ipropdata--imapiprop"></a>IPropData : IMAPIProp

  
  
**S’applique à** : Outlook 2013 | Outlook 2016 
  
Permet de récupérer et de modifier l’accès aux propriétés d’un objet. 
  
|Propriété|Valeur|
|:-----|:-----|
|Fichier d’en-tête :  <br/> |Mapiutil.h  <br/> |
|Exposé par :  <br/> |Objet de données de propriété  <br/> |
|Implémenté par :  <br/> |MAPI  <br/> |
|Appelé par :  <br/> |Fournisseurs de services et applications clientes  <br/> |
|Identificateur d’interface :  <br/> |IID_IMAPIPropData  <br/> |
|Type de pointeur :  <br/> |LPPROPDATA  <br/> |
|Modèle de transaction :  <br/> |Non transactionnel  <br/> |
   
## <a name="vtable-order"></a>Ordre des tables virtuelles

|Member|Description|
|:-----|:-----|
|[HrSetObjAccess](ipropdata-hrsetobjaccess.md) <br/> |D�finit le niveau d'acc�s de l'objet. |
|[HrSetPropAccess](ipropdata-hrsetpropaccess.md) <br/> |Définit le niveau d’accès et l’état d’une ou plusieurs propriétés de l’objet. |
|[HrGetPropAccess](ipropdata-hrgetpropaccess.md) <br/> |R�cup�re le niveau d'acc�s et l'�tat d'un ou plusieurs des propri�t�s de l'objet. |
|[HrAddObjProps](ipropdata-hraddobjprops.md) <br/> |Ajoute une ou plusieurs propriétés de type PT_OBJECT à l’objet. |
   
## <a name="remarks"></a>Remarques

L’interface **IPropData::IMAPIProp** est implémentée par MAPI et utilisée principalement par les fournisseurs de services qui accèdent à cette implémentation en appelant la fonction [CreateIProp](createiprop.md) . 
  
Pour plus d’informations sur les niveaux d’accès sur les objets et les propriétés, consultez [Autorisations pour les objets et les propriétés](permissions-for-mapi-objects-and-properties.md).
  
## <a name="see-also"></a>Voir aussi



[Interfaces MAPI](mapi-interfaces.md)

