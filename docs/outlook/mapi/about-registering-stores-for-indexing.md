---
title: À propos de l’inscription de magasins pour l’indexation
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
localization_priority: Normal
ms.assetid: dd2aa06a-96e8-1291-18b5-fc3c40b74e4d
description: Dernière modification le 09 mars 2015
ms.openlocfilehash: 195812f53c4c0aaf20e4ed6e215d15b0295c9a07
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/23/2018
ms.locfileid: "22584183"
---
# <a name="about-registering-stores-for-indexing"></a>À propos de l’inscription de magasins pour l’indexation

  
  
**S’applique à**: Outlook 2013 | Outlook 2016 
  
Cette rubrique est spécifique à la recherche instantanée dans Microsoft Office Outlook 2007.
  
Recherche instantanée vous permet de rechercher rapidement des éléments dans Outlook. Il utilise des composants de Windows Desktop Search.
  
Le Gestionnaire de protocole MAPI vérifie le Registre Windows pour les magasins il doit indexer à des fins de recherche. Fournisseurs de magasins indexer doivent être enregistrés dans le Registre Windows.
  
Par défaut, Windows Desktop Search ajoute quatre types de fournisseurs de magasins suivants dans le Registre Windows pour autoriser l’indexation :
  
- Magasin de fichiers de dossiers personnels (. (PST).
    
-  Banque d’informations Microsoft Exchange, y compris les fichiers du dossier en mode hors connexion (.ost). 
    
-  Banque de dossiers publics. 
    
-  Magasin pour Microsoft Office Outlook Connector pour MSN. 
    
 Fournisseurs de magasins tiers indexer doivent s’inscrire dans le Registre Windows. 
  
> [!NOTE]
> Les administrateurs et les utilisateurs peuvent utiliser un paramètre de stratégie de groupe pour empêcher l’indexation des éléments Outlook de Windows Desktop Search. Pour plus d’informations, voir [Extension de Windows Desktop Search](http://msdn.microsoft.com/library/2eab146a-8516-4b95-b73c-ca7f980ba233%28Office.15%29.aspx). 
  
## <a name="registry-keys"></a>Clés de Registre

Sur un ordinateur, tous les fournisseurs de banque indexer doivent être enregistrés sous un seul les trois clés de Registre suivantes dans le Registre Windows. Le Gestionnaire de protocole MAPI se présente sous chacune de ces clés dans l’ordre suivant :
  
1. \Software\Policies\Microsoft\Windows\Windows Search\ [HKLM]
    
2. \Software\Microsoft\Windows\Windows Search\Preferences\ [HKLM]
    
3. \Software\Microsoft\Windows\Windows Search\Preferences\ [HKCU]
    
 Chaque valeur sous la clé correspond à un fournisseur de magasins qui est indexé. Le nom de la valeur est le GUID (Globally Unique Identifier) du fournisseur de banque, qui est de type **DWORD** et a la valeur hexadécimale 0 x 00000001. 
  
## <a name="guids-for-store-providers"></a>GUID pour les fournisseurs de banque d’informations

La propriété MAPI **[PR_MDB_PROVIDER](pidtagstoreprovider-canonical-property.md)** Spécifie le GUID d’un magasin MAPI. Les GUID pour les fournisseurs de magasins qu’index Outlook sont décrits dans le tableau suivant. 
  
||||
|:-----|:-----|:-----|
|**Type du fournisseur de banque** <br/> |**GUID** <br/> |**Remarques** <br/> |
|Fichiers de dossiers personnels (. PST)  <br/> |{4154494E-BFF9-01B8-00AA-0037D96E0000}  <br/> |GUID est décrit en détail la mspst.h de fichier d’en-tête public **MSPST_UID_PROVIDER** <br/> |
|Exchange  <br/> |{C0A19454-7F29-1B10-A587-08002B2A2517}  <br/> |GUID est décrit en détail la edkmdb.h de fichier d’en-tête public **pbExchangeProviderPrimaryUserGuid** <br/> |
|Dossiers publics  <br/> |{70fab278-f7af-cd11-9bc8-00aa002fc45a}  <br/> |GUID est décrit en détail la edkmdb.h de fichier d’en-tête public **pbExchangeProviderPublicGuid** <br/> |
|Outlook Connector pour MSN  <br/> |{c34f5c97-eb05-bb4b-b199-2a7570ec7cf9}  <br/> |Aucun  <br/> |
   
## <a name="see-also"></a>Voir aussi



[À propos de l’API de magasin](about-the-store-api.md)

