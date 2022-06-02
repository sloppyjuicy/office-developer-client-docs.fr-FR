---
title: IProfAdmin IUnknown
description: Décrit les propriétés et l’ordre de tableau virtuel des membres pour IProfAdmin IUnknown, qui prend en charge l’administration des profils.
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
api_name:
- IProfAdmin
api_type:
- COM
ms.assetid: 274899cc-2894-4d99-84ec-f18121e856a0
ms.openlocfilehash: d1ce3c8ed8bed91655350b1b8b68d62d72016664
ms.sourcegitcommit: e2b79cc4469013a4b3705620a93aa70b88e6c996
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/02/2022
ms.locfileid: "65828051"
---
# <a name="iprofadmin--iunknown"></a>IProfAdmin : IUnknown

  
  
**S’applique à** : Outlook 2013 | Outlook 2016 
  
Prend en charge l’administration des profils. 
  
|Propriété|Valeur|
|:-----|:-----|
|Fichier d’en-tête :  <br/> |Mapix.h  <br/> |
|Exposé par :  <br/> |Objet d’administration de profil  <br/> |
|Implémenté par :  <br/> |MAPI  <br/> |
|Appelé par :  <br/> |Applications clientes  <br/> |
|Identificateur d’interface :  <br/> |IID_IProfAdmin  <br/> |
|Type de pointeur :  <br/> |LPPROFADMIN  <br/> |
   
## <a name="vtable-order"></a>Ordre des tables virtuelles

|Member|Description|
|:-----|:-----|
|[Getlasterror](iprofadmin-getlasterror.md) <br/> |Retourne une structure [MAPIERROR](mapierror.md) qui contient des informations sur l’erreur précédente qui s’est produite dans un objet d’administration de profil. |
|[GetProfileTable](iprofadmin-getprofiletable.md) <br/> |Fournit l’accès à la table de profils, une table qui contient des informations sur tous les profils disponibles. |
|[CreateProfile](iprofadmin-createprofile.md) <br/> |Crée un profil. |
|[DeleteProfile](iprofadmin-deleteprofile.md) <br/> |Supprime un profil. |
|[ChangeProfilePassword](iprofadmin-changeprofilepassword.md) <br/> |Déconseillé. Modifie le mot de passe d’un profil. |
|[CopyProfile](iprofadmin-copyprofile.md) <br/> |Copie un profil. |
|[RenameProfile](iprofadmin-renameprofile.md) <br/> |Attribue un nouveau nom à un profil. |
|[SetDefaultProfile](iprofadmin-setdefaultprofile.md) <br/> |Définit ou efface le profil par défaut d’un client. |
|[AdminServices](iprofadmin-adminservices.md) <br/> |Fournit l’accès à un objet d’administration de service de message pour apporter des modifications aux services de message dans un profil. |
   
## <a name="see-also"></a>Voir aussi



[Interfaces MAPI](mapi-interfaces.md)

