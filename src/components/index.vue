<template>
  <div>
    <div id="titre">
      <br>
      <h1>Facture</h1>
    </div>
    <div id="formulaire">
      <div class="partie1">
        <h1>Société</h1>
        <div class="container-fluid">
          <div class="row">
            <div class="col-auto">
              <label for="nomEntreprise" class="col-form-label">Nom de l'entreprise</label>
            </div>
            <div class="col-auto">
              <input type="text" id="nomEntreprise" v-model="nomEntreprise" class="form-control" required maxlength="50">
            </div>
          </div>
          <br>
        </div>
        <div class="container-fluid">
          <div class="row">
            <div class="col-auto">
              <label for="rue" class="col-form-label">Rue</label>
            </div>
            <div class="col-auto">
              <input type="text" id="rue" v-model="rue" class="form-control" required maxlength="50">
            </div>
          </div>
          <br>
        </div>
        <div class="container-fluid">
          <div class="row">
            <div class="col-auto">
              <label for="complement1" class="col-form-label">Complément 1</label>
            </div>
            <div class="col-auto">
              <input type="text" id="complement1" v-model="complement1" class="form-control" maxlength="50">
            </div>
          </div>
          <br>
        </div>
        <div class="container-fluid">
          <div class="row">
            <div class="col-auto">
              <label for="complement2" class="col-form-label">Complément 2</label>
            </div>
            <div class="col-auto">
              <input type="text" id="complement2" v-model="complement2" class="form-control" maxlength="50">
            </div>
          </div>
          <br>
        </div>
        <div class="container-fluid">
          <div class="row">
            <div class="col-auto">
              <label for="codePostal" class="col-form-label">Code postal</label>
            </div>
            <div class="col-auto">
              <input type="text" id="codePostal" v-model="codePostal" class="form-control" required maxlength="50">
            </div>
          </div>
        </div>
        <br>
        <div class="container-fluid">
          <div class="row">
            <div class="col-auto">
              <label for="telephone" class="col-form-label">Téléphone</label>
            </div>
            <div class="col-auto">
              <input type="text" id="telephone" v-model="telephone" class="form-control" required maxlength="50">
            </div>
          </div>
        </div>
        <br>
        <div class="container-fluid">
          <div class="row">
            <div class="col-auto">
              <label for="email" class="col-form-label">Email</label>
            </div>
            <div class="col-auto">
              <input type="email" id="email" v-model="email" class="form-control" required maxlength="50">
            </div>
          </div>
        </div>
      </div>

      <div class="partie2">
        <h1>Client</h1>
        <div class="container-fluid">
          <div class="row">
            <div class="col-auto">
              <label for="nomClient" class="col-form-label">Nom de l'entreprise</label>
            </div>
            <div class="col-auto">
              <input type="text" id="nomClient" v-model="nomClient" class="form-control" required maxlength="50">
            </div>
          </div>
          <br>
        </div>
        <div class="container-fluid">
          <div class="row">
            <div class="col-auto">
              <label for="rueClient" class="col-form-label">Rue</label>
            </div>
            <div class="col-auto">
              <input type="text" id="rueClient" v-model="rueClient" class="form-control" required maxlength="50">
            </div>
          </div>
          <br>
        </div>
        <div class="container-fluid">
          <div class="row">
            <div class="col-auto">
              <label for="complement1Client" class="col-form-label">Complément 1</label>
            </div>
            <div class="col-auto">
              <input type="text" id="complement1Client" v-model="complement1Client" class="form-control" maxlength="50">
            </div>
          </div>
          <br>
        </div>
        <div class="container-fluid">
          <div class="row">
            <div class="col-auto">
              <label for="complement2Client" class="col-form-label">Complément 2</label>
            </div>
            <div class="col-auto">
              <input type="text" id="complement2Client" v-model="complement2Client" class="form-control" maxlength="50">
            </div>
          </div>
          <br>
        </div>
        <div class="container-fluid">
          <div class="row">
            <div class="col-auto">
              <label for="codePostalClient" class="col-form-label">Code postal</label>
            </div>
            <div class="col-auto">
              <input type="text" id="codePostalClient" v-model="codePostalClient" class="form-control" required maxlength="50">
            </div>
          </div>
        </div>
        <br>
        <div class="container-fluid">
          <div class="row">
            <div class="col-auto">
              <label for="telephoneClient" class="col-form-label">Téléphone</label>
            </div>
            <div class="col-auto">
              <input type="text" id="telephoneClient" v-model="telephoneClient" class="form-control" required maxlength="50">
            </div>
          </div>
        </div>
        <br>
        <div class="container-fluid">
          <div class="row">
            <div class="col-auto">
              <label for="emailClient" class="col-form-label">Email</label>
            </div>
            <div class="col-auto">
              <input type="email" id="emailClient" v-model="emailClient" class="form-control" required maxlength="50">
            </div>
          </div>
        </div>
      </div>
    </div>

    <br>
    <br>
    <div id="total">
      <br>
      <h1>TOTAL de la facture</h1>
      <h1 id="total_prix">{{ totalPrix }} TTC</h1>
    </div>
    <br>
    <br>
    <div id="prix_total">
      <div class="parti1">
        <div class="container-fluid">
          <div class="row">
            <div class="col-auto">
              <label for="quantite" class="col-form-label">Quantité</label>
            </div>
            <div class="col-auto">
              <input type="text" id="quantite" v-model="quantite" class="form-control" required maxlength="50">
            </div>
          </div>
        </div>
        <br>
        <div class="container-fluid">
          <div class="row">
            <div class="col-auto">
              <label for="prixUniteTTC" class="col-form-label">Prix unité TTC</label>
            </div>
            <div class="col-auto">
              <input type="text" id="prixUniteTTC" v-model="prixUniteTTC" class="form-control" required maxlength="50">
            </div>
          </div>
        </div>
        <br>
        <div class="container-fluid">
          <div class="row">
            <div class="col-auto">
              <label for="tva" class="col-form-label">TVA %</label>
            </div>
            <div class="col-auto">
              <input type="text" id="tva" v-model="tva" class="form-control" required maxlength="50">
            </div>
          </div>
        </div>
      </div>

      <div class="parti2">
        <div class="container-fluid">
          <div class="row">
            <div class="col-auto">
              <label for="designationArticle" class="col-form-label">Désignation article</label>
            </div>
            <div class="col-auto">
              <input type="text" id="designationArticle" v-model="designationArticle" class="form-control" required maxlength="50">
            </div>
          </div>
        </div>
        <br>
        <div class="container-fluid">
          <div class="row">
            <div class="col-auto">
              <label for="reduction" class="col-form-label">Réduction</label>
            </div>
            <div class="col-auto">
              <input type="text" id="reduction" v-model="reduction" class="form-control" required maxlength="50">
            </div>
          </div>
        </div>
        <br>
        <div class="container-fluid">
          <div class="row">
            <div class="col-auto">
              <label for="dateFacture" class="col-form-label">Date facture</label>
            </div>
            <div class="col-auto">
              <input type="date" id="dateFacture" v-model="dateFacture" class="form-control" required maxlength="50">
            </div>
          </div>
        </div>
      </div>
    </div>
    <br>
    <br>
    <div id="ajouter">
      <div class="button">
        <button type="button" class="btn btn-light btn-lg btn-outline-dark" @click="ajouterArticle">Ajouter un article</button>
      </div>
    </div>

    <br>
    <br>
    <table class="table hover">
      <thead>
        <tr>
          <th scope="col">Quantité</th>
          <th scope="col">Désignation article</th>
          <th scope="col">Prix unité TTC</th>
          <th scope="col">Réduction</th>
          <th scope="col">TVA %</th>
          <th scope="col">Actions</th>
        </tr>
      </thead>
      <tbody id="table-body">
        <tr v-for="(article, index) in articles" :key="index">
          <td>{{ article.quantite }}</td>
          <td>{{ article.designationArticle }}</td>
          <td>{{ article.prixUniteTTC }}</td>
          <td>{{ article.reduction }}</td>
          <td>{{ article.tva }}</td>
          <td>
            <button class="btn btn-danger" @click="supprimerArticle(index)">Supprimer</button>
          </td>
        </tr>
      </tbody>
    </table>

    <br>

    <div id="cree_pdf">
      <div class="button">
        <button type="button" class="btn btn-info btn-lg btn-danger" @click="generatePDF()">Créer une facture</button>
      </div>
    </div>
  </div>
</template>

<script>
import jsPDF from 'jspdf';
import 'jspdf-autotable';

export default {
  data() {
    return {
      nomEntreprise: "",
      rue: "",
      complement1: "",
      complement2: "",
      codePostal: "",
      telephone: "",
      email: "",
      nomClient: "",
      rueClient: "",
      complement1Client: "",
      complement2Client: "",
      codePostalClient: "",
      telephoneClient: "",
      emailClient: "",
      quantite: "",
      designationArticle: "",
      prixUniteTTC: "",
      reduction: "",
      tva: "",
      dateFacture: "",
      articles: []
    };
  },
  computed: {
    totalPrix() {
      return this.articles.reduce((total, article) => {
        const quantite = parseFloat(article.quantite) || 0;
        const prixUniteTTC = parseFloat(article.prixUniteTTC) || 0;
        const reduction = parseFloat(article.reduction) || 0;
        const tva = parseFloat(article.tva) || 0;
        return total + (quantite * prixUniteTTC * (1 + tva / 100)) - reduction;
      }, 0).toFixed(2);
    }
  },
  methods: {
    ajouterArticle() {
      if (this.quantite && this.designationArticle && this.prixUniteTTC && this.reduction && this.tva) {
        this.articles.push({
          quantite: this.quantite,
          designationArticle: this.designationArticle,
          prixUniteTTC: this.prixUniteTTC,
          reduction: this.reduction,
          tva: this.tva
        });

        this.quantite = "";
        this.designationArticle = "";
        this.prixUniteTTC = "";
        this.reduction = "";
        this.tva = "";
      } else {
        alert("Tous les champs doivent être remplis");
      }
    },
    supprimerArticle(index) {
      this.articles.splice(index, 1);
    },generatePDF() {
  const doc = new jsPDF();

  // Titre de la facture
  doc.setFontSize(22);
  doc.text('Facture', 20, 20);

  // Informations sur la société
  doc.setFontSize(12);
  doc.text('De :', 20, 30);
  doc.text(this.nomEntreprise, 20, 35);
  doc.text(this.rue, 20, 40);
  if (this.complement1) doc.text(this.complement1, 20, 45);
  if (this.complement2) doc.text(this.complement2, 20, 50);
  doc.text(this.codePostal, 20, 55);
  doc.text(`Téléphone : ${this.telephone}`, 20, 60);
  doc.text(`Email : ${this.email}`, 20, 65);

  // Informations sur le client
  doc.text('Facturé à :', 120, 30);
  doc.text(this.nomClient, 120, 35);
  doc.text(this.rueClient, 120, 40);
  if (this.complement1Client) doc.text(this.complement1Client, 120, 45);
  if (this.complement2Client) doc.text(this.complement2Client, 120, 50);
  doc.text(this.codePostalClient, 120, 55);
  doc.text(`Téléphone : ${this.telephoneClient}`, 120, 60);
  doc.text(`Email : ${this.emailClient}`, 120, 65);

  // Date de la facture
  doc.text(`Date : ${this.dateFacture}`, 20, 75);

  // Tableau des articles
  const columns = ["Quantité", "Désignation", "Prix Unité TTC", "Réduction", "TVA"];
  const rows = this.articles.map(article => [
    article.quantite,
    article.designationArticle,
    article.prixUniteTTC,
    article.reduction,
    article.tva
  ]);

  doc.autoTable({
    startY: 85,
    head: [columns],
    body: rows,
    didDrawPage: (data) => {
      let finalY = data.cursor.y; // This will get the Y coordinate after autoTable
      // Total de la facture
      doc.setFontSize(16);
      doc.text(`Total : ${this.totalPrix} € TTC`, 20, finalY + 10);
    }
  });

  doc.save(`facture_${this.dateFacture}.pdf`);
}

    
  }
};
</script>

<style scoped>
#formulaire {
  display: flex;
  width: 100%;
  height: 90vh;
  justify-content: space-around;
  padding: 2px;
  padding-top: 8px;
  align-items: center;
}

#titre {
  display: flex;
  width: 100%;
  justify-content: center;
  padding-top: 8px;
}

#total {
  display: flex;
  width: 80%;
  justify-content: space-around;
  padding-top: 8px;
}

#prix_total {
  display: flex;
  width: 100%;
  justify-content: space-around;
  padding: 2px;
  padding-top: 8px;
  align-items: center;
}

#ajouter {
  display: flex;
  width: 100%;
  align-items: center;
  justify-content: center;
}
#cree_pdf {
  display: flex;
  width: 100%;
  align-items: center;
  justify-content: center;
}
</style>
