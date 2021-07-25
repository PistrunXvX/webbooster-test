<script lang="ts">
    import {
      Button,
      Modal,
      ModalBody,
      ModalFooter,
      ModalHeader,
      Input,
      FormGroup,
      Label,
      Form
    } from 'sveltestrap';
    let open = false;
    const toggle = () => (open = !open);
</script>  

<div class="cards">
    <div class="card__block">
        <img src="chear.jpg" alt="Парикмахерское кресло 'Норм' гидравлическое">
        <p class="card__text">
            Парикмахерское кресло <br> 
            'Норм' гидравлическое
        </p>
        <p class="card__price">
            9 990 ₽
        </p>
        <button on:click={toggle} class="card__button">
            Купить
        </button>
    </div>
    <Modal isOpen={open} {toggle}>
        <ModalHeader {toggle}>Форма обратной связи</ModalHeader>
        <ModalBody>
          <Form class="form" action="" id="data">
            <FormGroup>
                <Label>Имя</Label>
                <Input class="form__input" type="text" placeholder="Ваше имя" required></Input>
            </FormGroup>
            <FormGroup>
                <Label>Номер телефона</Label>
                <Input class="form__input" type="tel" placeholder="Ваш номер телефона" required></Input>
            </FormGroup>
            <FormGroup>
                <Label>Email</Label>
                <Input class="form__input" type="email" placeholder="Ваш email" required></Input>
            </FormGroup>
            <FormGroup>
                <Label>Товар</Label>
                <Input class="form__input" type="text" placeholder="Название товара" required></Input>
            </FormGroup>
        </Form>
        </ModalBody>
        <ModalFooter>
          <Button color="primary" form="data">Отправить</Button>
        </ModalFooter>
    </Modal>
</div>

<style>

    .cards {
        max-width: 30%;
        display: inline-block;
        text-align: center;
    }

    .card__block img{
        max-width: 30%;
    }

    .card__text{
        font-size: 14px;
    }

    .card__price {
        font-size: 18px;
        color: black;
        font-weight: bold;
    }

    .card__button{
        font-size: 14px;
        color: White;
        background-color: #f13c6e;
        border-radius: 20px;
        padding: 10px 40px;
        cursor: pointer;
    }



</style>