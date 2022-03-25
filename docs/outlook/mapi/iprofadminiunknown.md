---
title: IProfAdmin IUnknown
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
description: Dernière modification le 9 mars 2015
ms.openlocfilehash: aa2a46a561f4940ff92b438f010cc1fd01fa3e59
ms.sourcegitcommit: eb9453e5664b01759b602cb5a4cef5b4885128f3
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/24/2022
ms.locfileid: "63781711"
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
   
## <a name="vtable-order"></a>Ordre des vtables

|Member|Description|
|:-----|:-----|
|[GetLastError](iprofadmin-getlasterror.md) <br/> |Renvoie une structure [MAPIERROR](mapierror.md) qui contient des informations sur l’erreur précédente qui s’est produite sur un objet d’administration de profil. |
|[GetProfileTable](iprofadmin-getprofiletable.md) <br/> |Permet d’accéder à la table de profils, qui contient des informations sur tous les profils disponibles. |
|[CreateProfile](iprofadmin-createprofile.md) <br/> |Crée un profil. |
|[DeleteProfile](iprofadmin-deleteprofile.md) <br/> |Supprime un profil. |
|[ChangeProfilePassword](iprofadmin-changeprofilepassword.md) <br/> |Déconseillé. Modifie le mot de passe d’un profil. |
|[CopyProfile](iprofadmin-copyprofile.md) <br/> |Copie un profil. |
|[RenameProfile](iprofadmin-renameprofile.md) <br/> |Attribue un nouveau nom à un profil. |
|[SetDefaultProfile](iprofadmin-setdefaultprofile.md) <br/> |Définit ou effacer le profil par défaut d’un client. |
|[AdminServices](iprofadmin-adminservices.md) <br/> |Permet d’accéder à un objet d’administration de service de message pour apporter des modifications aux services de message dans un profil. |
   
## <a name="see-also"></a>Voir aussi



[Interfaces MAPI](mapi-interfaces.md)

