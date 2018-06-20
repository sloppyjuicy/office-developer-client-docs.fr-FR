---
title: Propriété canonique PidTagAddressBookChooseDirectoryAutomatically
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: cecd0679-4bc2-4399-8f89-a4e17bb909a0
description: 'Derni�re modification�: lundi 9 mars 2015'
ms.openlocfilehash: 48dfced07a8fd78a1af22679759effbd3c6da343
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19785679"
---
# <a name="pidtagaddressbookchoosedirectoryautomatically-canonical-property"></a>Propriété canonique PidTagAddressBookChooseDirectoryAutomatically

  
  
**S’applique à**: Outlook 
  
Permet à Microsoft Outlook 2010 et Microsoft Outlook 2013 de choisir la liste d’adresses globale (GAL) plus appropriée ou le dossier de contacts pour la boîte aux lettres en cours.
  
|||
|:-----|:-----|
|Propriétés associées :  <br/> |PR_AB_CHOOSE_DIRECTORY_AUTOMATICALLY  <br/> |
|Identificateur :  <br/> |0x3D1C000B  <br/> |
|Type de propriété :  <br/> |PT_BOOLEAN  <br/> |
|Zone :  <br/> |Carnet d’adresses  <br/> |
   
## <a name="remarks"></a>Remarques

Cette propriété correspond au paramètre **d’Accepter automatiquement** dans la boîte de dialogue Options de carnet d’adresses. Lorsque cette propriété existe dans la section profil IID_CAPONE_PROF et est définie sur **true**, le carnet d’adresses, boîte de dialogue par défaut, le conteneur spécifié par la méthode [SetDefaultDir](iaddrbook-setdefaultdir.md) n’est plus mais choisit un carnet d’adresses qui Outlook 2010 ou Outlook 2013 estime appropriée pour le contexte dans lequel la boîte de dialogue a été affiché. Notez que cela peut entraîner une mauvaise expérience pour les fournisseurs de carnet d’adresses tiers. 
  
## <a name="related-resources"></a>Ressources connexes

### <a name="header-files"></a>Fichiers d’en-tête

MAPITAGS.h
  
> Contient les définitions des propriétés répertoriées en tant que propriétés associées.
    
Mapidefs.h
  
> Fournit des définitions de type de données.
    
## <a name="see-also"></a>Voir aussi



[Propriétés MAPI](mapi-properties.md)
  
[Propriétés canoniques MAPI](mapi-canonical-properties.md)
  
[Constantes MAPI](mapi-constants.md)
  
[Mappage de noms de propriété canonique aux noms MAPI](mapping-canonical-property-names-to-mapi-names.md)
  
[Mappage de noms MAPI pour les noms de propriété canonique](mapping-mapi-names-to-canonical-property-names.md)

