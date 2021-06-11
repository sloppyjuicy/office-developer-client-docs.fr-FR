---
title: XML pour les amis
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: overview
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 3362639a-8098-47ab-ba94-ee89e4920032
description: L’élément friends du schéma XML du fournisseur Microsoft Outlook Social Connector (OSC) permet à un fournisseur OSC de spécifier des informations pour une liste de personnes associées à un utilisateur Outlook dans le réseau social.
ms.openlocfilehash: df3bf03c5fd1dcdac3096411bc60bcb1eeec661e
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32361158"
---
# <a name="xml-for-friends"></a>XML pour les amis

L’élément friends du schéma XML du fournisseur Microsoft Outlook Social Connector (OSC) permet à un fournisseur OSC de spécifier des informations pour une liste de personnes associées à un utilisateur Outlook dans le réseau social.  Si le fournisseur OSC prend en charge la synchronisation mise en cache, cette liste de personnes contient uniquement des amis de l’utilisateur Outlook sur le réseau social. Si OSC prend en charge la synchronisation à la demande ou hybride, cette liste peut contenir des amis et des non-amis de l’Outlook utilisateur. 

Chaque personne de la liste  est représentée en tant qu’élément de personne dans le schéma XML, qui prend en charge des détails tels que le prénom, le nom et les adresses e-mail. Les fournisseurs OSC  utilisent les éléments amis et personne, quelle que soit la façon dont ils souhaitent que l’OSC synchronise les informations d’amis à partir du réseau social.  Notez que les  éléments enfants de la personne sont similaires à certaines des propriétés d’un contact Outlook, ce qui facilite le stockage d’amis dans un dossier de contacts Outlook spécifique au réseau social, si le réseau social prend en charge la synchronisation mise en cache ou hybride des amis dans un dossier de contacts Outlook. 

## <a name="example-scenarios"></a>Exemples de scénarios

Les exemples de scénarios suivants illustrent les appels d’API d’extensibilité du fournisseur OSC qu’un fournisseur OSC implémente et l’OSC effectue pour obtenir des informations d’ami. Les informations sont exprimées dans des chaînes XML conformes au schéma XML du fournisseur OSC.
  
Pour obtenir un exemple de XML d’amis, voir [Friends XML Example](friends-xml-example.md). Pour plus d’informations sur la synchronisation des informations des amis, voir [Synchronizing Friends and Activities](synchronizing-friends-and-activities.md).

### <a name="scenario-1-get-a-list-of-friends"></a>Scénario 1 : obtenir une liste d’amis

Scénario 1 : OSC obtient une liste d’amis, un objet [ISocialPerson](isocialpersoniunknown.md) et une image pour chaque ami : 
    
1. Un fournisseur OSC qui prend en charge l’affichage des amis à partir du site de réseau social et permettant à l’OSC de mettre en cache des informations d’amis indique cela à l’OSC à l’aide des éléments **getFriends** et **cacheFriends,** qui sont des éléments enfants de l’élément **capabilities.** 
    
2. Le fournisseur OSC implémente également les méthodes [ISocialProvider::GetCapabilities,](isocialprovider-getcapabilities.md) [ISocialSession::GetPerson,](isocialsession-getperson.md) [ISocialPerson::GetFriendsAndColleagues](isocialperson-getfriendsandcolleagues.md)et [ISocialPerson::GetPicture.](isocialperson-getpicture.md) 
    
3. L’OSC appelle **ISocialProvider::GetCapabilities** pour vérifier la valeur des éléments suivants : **getFriends** pour vérifier que le fournisseur OSC prend en charge l’affichage des amis à partir du réseau social et **cacheFriends** pour vérifier que le fournisseur prend en charge la mise en cache des amis. 
    
4. L’OSC appelle **ISocialSession::GetPerson** pour obtenir un objet **ISocialPerson** pour l’Outlook utilisateur. 
    
5. L’OSC appelle **ISocialPerson::GetFriendsAndColleagues** pour obtenir la liste des amis de l’utilisateur Outlook renvoyée dans la chaîne de paramètre _personCollection._ La  _chaîne personCollection_ est conforme à la définition de schéma XML de l’élément **friends** dans le schéma XML. 
    
6. Pour chaque ami dans la chaîne XML  _personCollection,_ l’OSC obtient la valeur de l’élément **userID** pour appeler **ISocialSession::GetPerson** pour obtenir un objet **ISocialPerson** pour cet ami. 
    
7. Pour chaque ami dans la chaîne XML **personCollection,** l’OSC appelle [ISocialPerson::GetPicture](isocialperson-getpicture.md) pour obtenir une ressource d’image pour cet ami. 
    
   L’OSC peut effectuer d’autres appels sur l’objet **ISocialPerson** pour obtenir des activités et des détails (par exemple, des adresses e-mail) pour cet ami. 
    
### <a name="scenario-2-synchronize-friends"></a>Scénario 2 : synchroniser des amis 

Scénario 2 : OSC synchronise dynamiquement les amis :
    
1. Un fournisseur OSC qui prend en charge la synchronisation à la demande des amis et des non-amis indique cela à l’OSC à l’aide des éléments **getFriends** et **dynamicContactsLookup.** Le fournisseur OSC définit également **l’élément hashFunction.** Les trois éléments sont des éléments enfants **de fonctionnalités.** 
    
2. Le fournisseur OSC implémente également la [méthode ISocialSession2::GetPeopleDetails.](isocialsession2-getpeopledetails.md) 
    
3. L’OSC appelle **ISocialProvider::GetCapabilities** pour vérifier les valeurs de **getFriends** et **dynamicContactsLookup** pour vérifier que le fournisseur OSC prend en charge les amis et la synchronisation à la demande des amis et des non-amis. L’OSC note également la valeur de **hashFunction** prise en charge par le fournisseur OSC. 
    
4. Pour chaque utilisateur affiché dans le volet Personnes, l’OSC collecte l’adresse e-mail de l’utilisateur et la chiffre à l’aide de la fonction de hachage spécifiée dans **hashFunction**. Il s’agit d’une chaîne XML conforme à la définition de schéma XML de l’élément **hashedAddresses.** 
    
5. L’OSC appelle **ISocialSession2::GetPeopleDetails**, en fournissant cette chaîne XML d’adresses hachées en tant que paramètre _personAddresses,_ pour obtenir dynamiquement les détails mis à jour pour les personnes dans le paramètre _personsCollection._ La  _chaîne du paramètre personsCollection_ est conforme à la définition de schéma XML de l’élément **friends** dans le schéma XML. 

## <a name="parent-and-child-elements"></a>Éléments parents et enfants

Les éléments suivants sont les deux éléments de niveau supérieur dans **le schéma des** amis. 
  
|**Élément**|**Description**|
|:-----|:-----|
|**friends** <br/> |Représente l’élément racine d’une liste d’éléments **de** personne. Les éléments **ISocialPerson::GetFriendsAndColleagues,** [ISocialSession::FindPerson](isocialsession-findperson.md)et **ISocialSession2::GetPeopleDetails** retournent des chaînes XML conformes à la définition de schéma de l’élément **friends.**  <br/> |
|**person** <br/> |Représente une personne dans une liste d’éléments **de** personne. La [méthode ISocialPerson::GetDetails](isocialperson-getdetails.md) renvoie une chaîne XML conforme à la définition de schéma de l’élément **de** personne.  <br/> |
   
Le tableau suivant décrit chaque élément enfant de l’élément **person** dans le schéma XML du fournisseur OSC. 
  
Pour obtenir une définition complète du schéma XML du fournisseur OSC, y compris les éléments requis ou facultatifs, voir Outlook [Social Connector Provider XML Schema](outlook-social-connector-provider-xml-schema.md).
  
|**Élément**|**Description**|
|:-----|:-----|
|**adresse** <br/> |Adresse de rue physique de la personne.  <br/> |
|**anniversary** <br/> |Date anniversaire d’un événement pour la personne.  <br/> |
|**askmeabout** <br/> |Rubriques d’intérêt ou d’expertise de la personne.  <br/> |
|**birthday** <br/> |Date de naissance de la personne.  <br/> |
|**businessAddress** <br/> |Adresse de rue physique de l’espace de travail de la personne.  <br/> |
|**businessCity** <br/> |Ville de l’espace de travail de la personne.  <br/> |
|**businessCountryOrRegion** <br/> |Pays ou région de l’espace de travail de la personne.  <br/> |
|**businessState** <br/> |Département ou province de l’espace de travail de la personne.  <br/> |
|**businessZip** <br/> |Code postal ou postal de l’espace de travail de la personne.  <br/> |
|**cell** <br/> |Numéro de téléphone mobile de la personne.  <br/> |
|**Ville** <br/> |Ville de l’adresse physique de la personne.  <br/> |
|**company** <br/> |Nom de la société associée à la personne.  <br/> |
|**countryOrRegion** <br/> |Pays ou région de l’adresse physique de la personne.  <br/> |
|**creationTime** <br/> |Heure de création du profil de la personne sur le réseau social.  <br/> |
|**emailAddress** <br/> |Adresse de messagerie principale de la personne.  <br/> |
|**emailAddress2** <br/> |Adresse de messagerie secondaire de la personne.  <br/> |
|**emailAddress3** <br/> |Adresse de messagerie troisième de la personne.  <br/> |
|**expirationTime** <br/> |Heure d’expiration des données de profil de la personne sur le réseau social.  <br/> |
|**fileAs** <br/> |Chaîne par laquelle la personne doit être classée en tant que contact dans un fichier Outlook contacts.  <br/> |
|**firstName** <br/> |Prénom ou prénom de la personne.  <br/> |
|**friendStatus** <br/> |Statut d’ami de cette personne avec l’utilisateur connecté sur le réseau social. Doit être l’une des valeurs suivantes : **friend**, **nonfriend**, **pendingin**, **pendingout**.   <br/> |
|**fullName** <br/> |Nom complet de la personne.  <br/> |
|**gender** <br/> |Sexe de la personne. Doit être l’une des valeurs suivantes : **male**, **female**, **unspecified**.  <br/> |
|**homePhone** <br/> |Numéro de téléphone de la personne.  <br/> |
|**index** <br/> |Emplacement de l’adresse hachée de la personne dans le paramètre de chaîne _personsAddresses_ transmis à un appel à la méthode **ISocialSession2::GetPeopleDetails.** Il indique également le **XML** de personne de la personne dans la chaîne  _personsCollection renvoyée_ par **GetPeopleDetails**.  <br/> |
|**secteurs d’activité** <br/> |Les secteurs d’activité de la personne.  <br/> |
|**interests** <br/> |Centres d’intérêt ou loisirs de la personne.  <br/> |
|**lastModificationTime** <br/> |Heure de la dernière modification du profil de la personne sur le réseau social.  <br/> |
|**lastName** <br/> |Nom ou nom de famille de la personne.  <br/> |
|**location** <br/> |Emplacement de la personne.  <br/> |
|**nickname** <br/> |Nom plus court ou nom de la personne qui a été créé.  <br/> |
|**otherAddress** <br/> |Autre adresse de rue de la personne.  <br/> |
|**otherCity** <br/> |Ville de l’adresse alternative de la personne.  <br/> |
|**otherCountryOrRegion** <br/> |Pays ou région de l’adresse alternative de la personne.  <br/> |
|**otherState** <br/> |Département ou province de l’adresse alternative de la personne.  <br/> |
|**otherZip** <br/> |Code postal ou postal de l’adresse alternative de la personne.  <br/> |
|**téléphone** <br/> |Numéro de téléphone du contact principal de la personne.  <br/> |
|**pictureUrl** <br/> |URL d’une image de profil de la personne.  <br/> |
|**relation** <br/> |Relation de cette personne avec l’utilisateur connecté.  <br/> |
|**schools** <br/> |Les écoles vers qui la personne va ou s’est rendu.  <br/> |
|**skills** <br/> |Compétences personnelles de la personne.  <br/> |
|**state** <br/> |Département ou province de l’adresse physique de la personne.  <br/> |
|**title** <br/> |Désignation ajoutée au nom de la personne.  <br/> |
|**userID** <br/> |ID permettant d’identifier la personne sur le réseau social.  <br/> |
|**webProfilePage** <br/> |Adresse de page web qui contient un profil de la personne.  <br/> |
|**site web** <br/> |Site web de la personne.  <br/> |
|**workPhone** <br/> |Numéro de téléphone d’entreprise de la personne.  <br/> |
|**zip** <br/> |Code postal ou code postal de l’adresse physique de la personne.  <br/> |
   
## <a name="see-also"></a>Voir aussi

- [Exemple XML Friends](friends-xml-example.md)  
- [Synchronisation des amis et des activités](synchronizing-friends-and-activities.md)  
- [XML pour les fonctionnalités](xml-for-capabilities.md) 
- [XML pour les activités](xml-for-activities.md)
- [Développement d'un fournisseur avec le schéma XML OSC](developing-a-provider-with-the-osc-xml-schema.md)

