---
title: Identificateurs d’entrée ponctuelle
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.localizationpriority: medium
api_type:
- COM
ms.assetid: 741d21ae-f14a-4b7f-80aa-91d0f0ff3f34
ms.openlocfilehash: 2379d47773ea245c8be13c80bf3df57380423953
ms.sourcegitcommit: 518845d053a009b11c8d907a33822161c0b6bc96
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/08/2022
ms.locfileid: "63369300"
---
# <a name="one-off-entry-identifiers"></a>Identificateurs d’entrée ponctuelle
  
**S’applique à** : Outlook 2013 | Outlook 2016 
  
Les identificateurs d’entrée uniques sont créés par MAPI dans la méthode **IAddrBook::CreateOneOff** et par des composants qui n’ont pas accès au sous-système MAPI, tels que les composants de passerelle. For more information, see [IAddrBook::CreateOneOff](iaddrbook-createoneoff.md). L’illustration suivante montre le format d’un identificateur d’entrée unique.
  
**Format d’identificateur d’entrée unique**
  
![Format d’identificateur d’entrée unique](media/amapi_69.gif "Format d’identificateur d’entrée unique")
  
Le premier champ est une structure [MAPIUID](mapiuid.md) spéciale qui identifie l’identificateur d’entrée comme représentant un destinataire personnalisé. Cette structure **MAPIUID** doit être définie sur la constante MAPI_ONE_OFF_UID. MAPI_ONE_OFF_UID est défini dans le fichier d’en-tête MAPIDEFS.H. 
  
Les champs version et indicateurs sont des mots 16 bits dans l’ordre des byte Intel. Le champ version doit avoir la valeur zéro. Le champ indicateurs peut être définie sur les valeurs suivantes :
  
MAPI_ONE_OFF_NO_RICH_INFO
  
MAPI_ONE_OFF_UNICODE
  
L MAPI_ONE_OFF_NO_RICH_INFO est définie si un destinataire ne doit pas recevoir de contenu de message au format TNEF (Transport Neutral Encapsulation Format). Cet indicateur est définie lorsque MAPI_SEND_NO_RICH_INFO est transmis à [la méthode IAddrBook::CreateOneOff](iaddrbook-createoneoff.md) . 
  
L MAPI_ONE_OFF_UNICODE est définie si le nom d’affichage et l’adresse e-mail sont des chaînes Unicode. Cet indicateur est définie lorsque le MAPI_UNICODE est transmis à **IAddrBook::CreateOneOff**. Lorsque l’indicateur MAPI_UNICODE n’est pas transmis à **CreateOneOff**, MAPI suppose que le nom complet et les chaînes d’adresse de messagerie se trouve dans le jeu de caractères ANSI actuel de la station de travail. Les chaînes ANSI ne fonctionnent généralement pas bien dans les messages envoyés entre les plateformes à l’aide de jeux de caractères différents, car la page de code n’est pas codée dans l’identificateur d’entrée. Pour se protéger contre cette incompatibilité potentielle, de nombreux types d’adresses sont limités uniquement aux caractères communs à plusieurs jeux de caractères. Toutefois, pour garantir la compatibilité du jeu de caractères et de la plateforme, les clients doivent utiliser Unicode pour les chaînes de caractères dans leurs messages.
  
Le nom complet est une chaîne terminée par null qui correspond à la propriété **PR_DISPLAY_NAME** ([PidTagDisplayName](pidtagdisplayname-canonical-property.md)) du destinataire et au paramètre  _lpszName_ transmis à **IAddrBook::CreateOneOff**. Le jeu de caractères est Unicode si l’MAPI_ONE_OFF_UNICODE est définie et ANSI s’il est clair. 
  
Le type d’adresse est une chaîne terminée par null qui correspond à la propriété **PR_ADDRTYPE** ([PidTagAddressType](pidtagaddresstype-canonical-property.md)) du destinataire et au paramètre  _lpszAdrType_ transmis à **IAddrBook::CreateOneOff**. 
  
L’adresse e-mail est une chaîne terminée par null qui correspond à la propriété **PR_EMAIL_ADDRESS** ([PidTagEmailAddress](pidtagemailaddress-canonical-property.md)) du destinataire et au paramètre  _lpszAddress_ transmis à **IAddrBook::CreateOneOff**. 
  
> [!NOTE]
> Il n’existe aucun remplissage dans les structures d’identificateur d’entrée uniques ; les octets sont packés exactement comme indiqué ci-dessus et la longueur de l’identificateur d’entrée ne doit pas inclure d’octets au-delà du caractère null de fin de l’adresse e-mail. 
  
Les clients et les fournisseurs de carnet d’adresses qui créent manuellement des identificateurs d’entrée uniques peuvent également avoir besoin de générer des valeurs pour les propriétés **PR_RECORD_KEY** ([PidTagRecordKey](pidtagrecordkey-canonical-property.md)) et **PR_SEARCH_KEY** ([PidTagSearchKey](pidtagsearchkey-canonical-property.md)). La clé d’enregistrement est identique à l’identificateur d’entrée. La clé de recherche doit être formée en concassant les champs suivants dans l’ordre suivant :
  
1. Type d’adresse, converti en caractères en minuscules.
    
2. Deux-points (:).
    
3. Adresse de messagerie, convertie en caractères en minuscules.
    
4. Caractère null de fin.
    
Aucune conversion de jeu de caractères ne doit être effectuée lors de la génération de la clé de recherche.
  

