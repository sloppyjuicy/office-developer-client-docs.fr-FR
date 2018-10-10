---
title: Jeux d'enregistrements hiérarchiques dans XML
TOCTitle: Hierarchical Recordsets in XML
ms:assetid: 606dee87-8762-6cc2-a151-94d34031b35f
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249351(v=office.15)
ms:contentKeyID: 48545181
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 1f608cd8ed36b621847c58dd523cfa052c5f501a
ms.sourcegitcommit: 19aca09c5812cfb98b68b5d4604dcaa814479df7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 10/09/2018
ms.locfileid: "25471473"
---
# <a name="hierarchical-recordsets-in-xml"></a>Jeux d'enregistrements hiérarchiques dans XML


**S’applique à**: Access 2013 | Office 2013

## <a name="hierarchical-recordsets-in-xml"></a>Jeux d'enregistrements hiérarchiques dans XML

ADO autorise la persistance des objets **Recordset** hiérarchiques au format XML. Avec les objets **Recordset** hiérarchiques, la valeur d’un champ dans **l’objet Recordset** parent est un autre **jeu d’enregistrements**. Ces champs sont représentées comme éléments enfants dans le flux XML plutôt qu’un attribut. L’exemple suivant illustre ce cas :

```vb 
 
Rs.Open "SHAPE {select stor_id, stor_name, state from stores} APPEND ({select stor_id, ord_num, ord_date, qty from sales} AS rsSales RELATE stor_id TO stor_id)", "Provider=MSDataShape;DSN=pubs;UID=MyUserId;PWD=MyPassword;" 
```

L'exemple suivant représente le format XML du **jeu d'enregistrements** persistant :

```xml 
 
<xml xmlns:s="uuid:BDC6E3F0-6DA3-11d1-A2A3-00AA00C14882"     xmlns:dt="uuid:C2F41010-65B3-11d1-A29F-00AA00C14882"     xmlns:rs="urn:schemas-microsoft-com:rowset"  
    xmlns:z="#RowsetSchema">  
  <s:Schema id="RowsetSchema">  
    <s:ElementType name="row" content="eltOnly" rs:updatable="true">  
      <s:AttributeType name="stor_id" rs:number="1"  
        rs:writeunknown="true">  
        <s:datatype dt:type="string" dt:maxLength="4"  
          rs:fixedlength="true" rs:maybenull="false"/>  
      </s:AttributeType>  
      <s:AttributeType name="stor_name" rs:number="2" rs:nullable="true"  
        rs:writeunknown="true">  
          <s:datatype dt:type="string" dt:maxLength="40"/>  
      </s:AttributeType>  
      <s:AttributeType name="state" rs:number="3" rs:nullable="true"  
        rs:writeunknown="true">  
        <s:datatype dt:type="string" dt:maxLength="2"  
          rs:fixedlength="true"/>  
      </s:AttributeType>  
      <s:ElementType name="rsSales" content="eltOnly"  
        rs:updatable="true" rs:relation="010000000100000000000000">  
        <s:AttributeType name="stor_id" rs:number="1"  
          rs:writeunknown="true">  
          <s:datatype dt:type="string" dt:maxLength="4"  
            rs:fixedlength="true" rs:maybenull="false"/>  
        </s:AttributeType>  
        <s:AttributeType name="ord_num" rs:number="2"  
          rs:writeunknown="true">  
          <s:datatype dt:type="string" dt:maxLength="20"  
            rs:maybenull="false"/>  
        </s:AttributeType>  
        <s:AttributeType name="ord_date" rs:number="3"  
          rs:writeunknown="true">  
            <s:datatype dt:type="dateTime" dt:maxLength="16"  
              rs:scale="3" rs:precision="23" rs:fixedlength="true"  
              rs:maybenull="false"/>  
        </s:AttributeType>  
        <s:AttributeType name="qty" rs:number="4" rs:writeunknown="true">  
          <s:datatype dt:type="i2" dt:maxLength="2" rs:precision="5"  
            rs:fixedlength="true" rs:maybenull="false"/>  
        </s:AttributeType>  
        <s:extends type="rs:rowbase"/>  
      </s:ElementType>  
      <s:extends type="rs:rowbase"/>  
    </s:ElementType>  
  </s:Schema>  
  <rs:data>  
    <z:row stor_id="6380" stor_name="Eric the Read Books" state="WA">  
      <rsSales stor_id="6380" ord_num="6871"  
        ord_date="1994-09-14T00:00:00" qty="5"/>  
      <rsSales stor_id="6380" ord_num="722a"  
        ord_date="1994-09-13T00:00:00" qty="3"/>  
    </z:row>  
    <z:row stor_id="7066" stor_name="Barnum's" state="CA">  
      <rsSales stor_id="7066" ord_num="A2976"  
        ord_date="1993-05-24T00:00:00" qty="50"/>  
      <rsSales stor_id="7066" ord_num="QA7442.3"  
        ord_date="1994-09-13T00:00:00" qty="75"/>  
    </z:row>  
    <z:row stor_id="7067" stor_name="News & Brews" state="CA">  
      <rsSales stor_id="7067" ord_num="D4482"  
        ord_date="1994-09-14T00:00:00" qty="10"/>  
      <rsSales stor_id="7067" ord_num="P2121"  
        ord_date="1992-06-15T00:00:00" qty="40"/>  
      <rsSales stor_id="7067" ord_num="P2121"  
        ord_date="1992-06-15T00:00:00" qty="20"/>  
      <rsSales stor_id="7067" ord_num="P2121"  
        ord_date="1992-06-15T00:00:00" qty="20"/>  
    </z:row>  
... 
  </rs:data>  
</xml>  
```

L'ordre exact des colonnes du **jeu d'enregistrements** parent n'est pas évident lorsqu'il est conservé de cette manière. Tout champ du parent peut contenir un **jeu d'enregistrements** enfant. Le fournisseur de persistance conserve d'abord toutes les colonnes scalaires en tant qu'attributs, puis toutes les « colonnes » du **jeu d'enregistrements** enfant comme des éléments enfants de la ligne parent. Vous pouvez obtenir la position ordinale du champ du **jeu d'enregistrements** en consultant la définition schématique du **jeu d'enregistrements**. Chaque champ comprend une propriété OLE DB, **rs:number**, définie dans l'espace de noms du schéma **Recordset** qui contient le nombre ordinal de ce champ.

Les noms de tous les champs du **jeu d'enregistrements** enfant sont concaténés avec le nom du champ du **jeu d'enregistrements** parent dont il dépend. Ceci permet d'éviter les conflits de noms dans les cas où les **jeux d'enregistrements** enfant et parent contiennent tous les deux un champ obtenu à partir de deux tables différentes mais portant le même nom.

Lorsque vous enregistrez des **jeux d'enregistrements** hiérarchiques au format XML, gardez à l'esprit les restrictions suivantes dans ADO :

  - Un **jeu d'enregistrements** hiérarchique avec des mises à jour en suspens ne peut pas être conservé au format XML.

  - Un **jeu d'enregistrements** hiérarchique créé avec une commande de mise en forme paramétrée ne peut pas être conservé (que ce soit au format XML ou ADTG).

  - ADO enregistre actuellement la relation entre les **jeux d'enregistrements** enfant et parent en tant que BLOB. Les balises XML décrivant cette relation ne sont pas encore définies dans l'espace de noms du schéma du jeu de lignes.

  - Lorsque vous sauvegardez un **jeu d'enregistrements** hiérarchique, tous les **jeux d'enregistrements** enfants sont sauvegardés en même temps. Si le **jeu d'enregistrements** actif dépend d'un autre **jeu d'enregistrements**, son parent n'est pas sauvegardé. Tous les **jeux d'enregistrements** enfants formant une sous-arborescence du **jeu d'enregistrements** actif sont sauvegardés.

Lorsque vous rouvrez un **jeu d'enregistrements** à partir de son format de persistance XML, gardez à l'esprit les restrictions suivantes :

  - Si l'enregistrement enfant contient des enregistrements n'ayant pas d'enregistrements parents associés, les lignes correspondantes n'apparaissent pas dans la représentation XML du **jeu d'enregistrements** hiérarchique. Par conséquent, ces lignes sont perdues lorsque le **jeu d'enregistrements** est réouvert à partir de son emplacement de persistance.

  - Si un enregistrement enfant est lié à plusieurs enregistrements parent, puis rouvrez le **jeu d’enregistrements**, **l’objet Recordset** enfant peut contenir les enregistrements en double. Toutefois, ces doublons ne seront visibles que si l’utilisateur travaille directement avec l’ensemble de lignes enfant sous-jacent. Si un chapitre est utilisé pour parcourir le **jeu d’enregistrements** (c’est le seul moyen pour naviguer dans ADO) enfant, les doublons ne sont pas visibles.

