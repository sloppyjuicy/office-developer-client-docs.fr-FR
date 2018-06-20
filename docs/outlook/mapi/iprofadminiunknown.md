---
title: IProfAdmin IUnknown
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IProfAdmin
api_type:
- COM
ms.assetid: 274899cc-2894-4d99-84ec-f18121e856a0
description: 'Derni�re modification�: lundi 9 mars 2015'
ms.openlocfilehash: c6192e6f92078f2f9bab0d55e9952d21ebb82af6
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19784382"
---
# <a name="iprofadmin--iunknown"></a>IProfAdmin : IUnknown

  
  
**S’applique à**: Outlook 
  
Prend en charge l’administration des profils. 
  
|||
|:-----|:-----|
|Fichier d’en-tête :  <br/> |MAPIX.h  <br/> |
|Exposés par :  <br/> |Objet d’administration de profil  <br/> |
|Implémentée par :  <br/> |MAPI  <br/> |
|Appelée par :  <br/> |Applications clientes  <br/> |
|Identificateur de l’interface :  <br/> |IID_IProfAdmin  <br/> |
|Type de pointeur :  <br/> |LPPROFADMIN  <br/> |
   
## <a name="vtable-order"></a>Ordre vtable

|||
|:-----|:-----|
|[GetLastError](iprofadmin-getlasterror.md) <br/> |Retourne une structure [MAPIERROR](mapierror.md) qui contient des informations sur l’erreur précédente s’est produite pour un objet d’administration de profil.  <br/> |
|[GetProfileTable](iprofadmin-getprofiletable.md) <br/> |Permet d’accéder à la table de profil, un tableau qui contient des informations sur tous les profils disponibles.  <br/> |
|[CreateProfile](iprofadmin-createprofile.md) <br/> |Crée un nouveau profil.  <br/> |
|[DeleteProfile](iprofadmin-deleteprofile.md) <br/> |Supprime un profil.  <br/> |
|[ChangeProfilePassword](iprofadmin-changeprofilepassword.md) <br/> |Déconseillé. Modifie le mot de passe pour un profil.  <br/> |
|[CopyProfile](iprofadmin-copyprofile.md) <br/> |Copie d’un profil.  <br/> |
|[RenameProfile](iprofadmin-renameprofile.md) <br/> |Affecte un nouveau nom à un profil.  <br/> |
|[SetDefaultProfile](iprofadmin-setdefaultprofile.md) <br/> |Active ou désactive le profil par défaut d’un client.  <br/> |
|[AdminServices](iprofadmin-adminservices.md) <br/> |Donne accès à un objet de l’administration de service de message pour apporter des modifications aux services de message dans un profil.  <br/> |
   
## <a name="see-also"></a>Voir aussi



[Interfaces MAPI](mapi-interfaces.md)

