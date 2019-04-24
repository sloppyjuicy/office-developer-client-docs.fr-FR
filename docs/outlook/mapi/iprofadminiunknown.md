---
title: /IUnknown IProfAdmin
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
ms.openlocfilehash: cbdfba68490b1e756f277c6e552235368a86f310
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32348852"
---
# <a name="iprofadmin--iunknown"></a>IProfAdmin : IUnknown

  
  
**S’applique à** : Outlook 2013 | Outlook 2016 
  
Prend en charge l'administration des profils. 
  
|||
|:-----|:-----|
|Fichier d’en-tête :  <br/> |Mapix. h  <br/> |
|Exposé par:  <br/> |Objet d'administration des profils  <br/> |
|Implémenté par :  <br/> |MAPI  <br/> |
|Appelé par :  <br/> |Applications clientes  <br/> |
|Identificateur de l'interface:  <br/> |IID_IProfAdmin  <br/> |
|Type de pointeur:  <br/> |LPPROFADMIN  <br/> |
   
## <a name="vtable-order"></a>Ordre vtable

|||
|:-----|:-----|
|[Généré](iprofadmin-getlasterror.md) <br/> |Renvoie une structure [MAPIERROR](mapierror.md) qui contient des informations sur l'erreur précédente qui s'est produite sur un objet d'administration de profil.  <br/> |
|[GetProfileTable](iprofadmin-getprofiletable.md) <br/> |Fournit l'accès à la table de profils, une table qui contient des informations sur tous les profils disponibles.  <br/> |
|[CreateProfile](iprofadmin-createprofile.md) <br/> |Crée un nouveau profil.  <br/> |
|[DeleteProfile](iprofadmin-deleteprofile.md) <br/> |Supprime un profil.  <br/> |
|[ChangeProfilePassword](iprofadmin-changeprofilepassword.md) <br/> |Déconseillé. Modifie le mot de passe d'un profil.  <br/> |
|[CopyProfile](iprofadmin-copyprofile.md) <br/> |Copie un profil.  <br/> |
|[RenameProfile](iprofadmin-renameprofile.md) <br/> |Affecte un nouveau nom à un profil.  <br/> |
|[SetDefaultProfile](iprofadmin-setdefaultprofile.md) <br/> |Définit ou efface le profil par défaut d'un client.  <br/> |
|[AdminServices](iprofadmin-adminservices.md) <br/> |Permet d'accéder à un objet d'administration de service de messagerie pour apporter des modifications aux services de messagerie dans un profil.  <br/> |
   
## <a name="see-also"></a>Voir aussi



[Interfaces MAPI](mapi-interfaces.md)

