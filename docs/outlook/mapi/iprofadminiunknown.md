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
ms.openlocfilehash: a6387de14e7b4ee513168ddd65383c39481c8699
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/24/2021
ms.locfileid: "59620575"
---
# <a name="iprofadmin--iunknown"></a>IProfAdmin : IUnknown

  
  
**S’applique à** : Outlook 2013 | Outlook 2016 
  
Prend en charge l’administration des profils. 
  
|||
|:-----|:-----|
|Fichier d’en-tête :  <br/> |Mapix.h  <br/> |
|Exposé par :  <br/> |Objet d’administration de profil  <br/> |
|Implémenté par :  <br/> |MAPI  <br/> |
|Appelé par :  <br/> |Applications clientes  <br/> |
|Identificateur d’interface :  <br/> |IID_IProfAdmin  <br/> |
|Type de pointeur :  <br/> |LPPROFADMIN  <br/> |
   
## <a name="vtable-order"></a>Ordre des vtables

|||
|:-----|:-----|
|[GetLastError](iprofadmin-getlasterror.md) <br/> |Renvoie une structure [MAPIERROR](mapierror.md) qui contient des informations sur l’erreur précédente qui s’est produite sur un objet d’administration de profil.  <br/> |
|[GetProfileTable](iprofadmin-getprofiletable.md) <br/> |Permet d’accéder à la table de profils, qui contient des informations sur tous les profils disponibles.  <br/> |
|[CreateProfile](iprofadmin-createprofile.md) <br/> |Crée un profil.  <br/> |
|[DeleteProfile](iprofadmin-deleteprofile.md) <br/> |Supprime un profil.  <br/> |
|[ChangeProfilePassword](iprofadmin-changeprofilepassword.md) <br/> |Déconseillé. Modifie le mot de passe d’un profil.  <br/> |
|[CopyProfile](iprofadmin-copyprofile.md) <br/> |Copie un profil.  <br/> |
|[RenameProfile](iprofadmin-renameprofile.md) <br/> |Attribue un nouveau nom à un profil.  <br/> |
|[SetDefaultProfile](iprofadmin-setdefaultprofile.md) <br/> |Définit ou définit le profil par défaut d’un client.  <br/> |
|[AdminServices](iprofadmin-adminservices.md) <br/> |Permet d’accéder à un objet d’administration de service de message pour apporter des modifications aux services de message dans un profil.  <br/> |
   
## <a name="see-also"></a>Voir aussi



[Interfaces MAPI](mapi-interfaces.md)

