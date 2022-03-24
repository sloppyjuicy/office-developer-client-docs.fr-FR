---
title: Propriété canonique PidTagAddressBookChooseDirectoryAutomatically
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
ms.assetid: cecd0679-4bc2-4399-8f89-a4e17bb909a0
description: Permet aux Microsoft Outlook 2010 et Microsoft Outlook 2013 de choisir le dossier de contacts ou la plus appropriée pour la boîte aux lettres active.
ms.openlocfilehash: daa6bd010728d4d9f19254567465f528b21b3ce0
ms.sourcegitcommit: 0a067f44281eddabff15fff565fb80eaa543b660
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/23/2022
ms.locfileid: "63763123"
---
# <a name="pidtagaddressbookchoosedirectoryautomatically-canonical-property"></a>Propriété canonique PidTagAddressBookChooseDirectoryAutomatically

  
  
**S’applique à** : Outlook 2013 | Outlook 2016 
  
Permet aux Microsoft Outlook 2010 et Microsoft Outlook 2013 choisir le dossier de contacts ou la liste d’adresses globale le plus approprié pour la boîte aux lettres active.
  
|Propriété |Valeur |
|:-----|:-----|
|Propriétés associées :  <br/> |PR_AB_CHOOSE_DIRECTORY_AUTOMATICALLY  <br/> |
|Identificateur :  <br/> |0x3D1C000B  <br/> |
|Type de propriété :  <br/> |PT_BOOLEAN  <br/> |
|Domaine :  <br/> |Carnet d’adresses  <br/> |
   
## <a name="remarks"></a>Remarques

Cette propriété correspond au paramètre **Choisir** automatiquement dans la boîte de dialogue Options du carnet d’adresses. Lorsque cette propriété existe dans la section profil IID_CAPONE_PROF et est définie sur **true**, la boîte de dialogue carnet d’adresses n’est plus définie par défaut sur le conteneur spécifié par la méthode [SetDefaultDir](iaddrbook-setdefaultdir.md), mais choisit un carnet d’adresses que Outlook 2010 ou Outlook 2013 considère comme approprié pour le contexte dans lequel la boîte de dialogue a été affichée. Notez que cela peut entraîner une expérience médiocre pour les fournisseurs de carnets d’adresses tiers. 
  
## <a name="related-resources"></a>Ressources connexes

### <a name="header-files"></a>Fichiers d’en-tête

Mapitags.h
  
> Contient les définitions des propriétés répertoriées en tant que propriétés associées.
    
Mapidefs.h
  
> Fournit des définitions de type de données.
    
## <a name="see-also"></a>Voir aussi



[Propriétés MAPI](mapi-properties.md)
  
[Propriétés canoniques MAPI](mapi-canonical-properties.md)
  
[Constantes MAPI](mapi-constants.md)
  
[Mappage des noms de propriétés canoniques aux noms MAPI](mapping-canonical-property-names-to-mapi-names.md)
  
[Mappage des noms MAPI aux noms de propriétés canoniques](mapping-mapi-names-to-canonical-property-names.md)

